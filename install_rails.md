﻿<!DOCTYPE html>
<html lang="en">
<body>
  <h1>How to Install Ruby on Rails</h1>
  <p>To install Ruby on Rails on your machine, follow these steps. The process varies slightly depending on your operating system (Windows, macOS, or Linux). Below is a general guide:</p>

  <h2>1. Install Ruby</h2>
  <p>Ruby on Rails requires Ruby to be installed first. The recommended version is Ruby 3.x.</p>

  <h3>macOS</h3>
  <ol>
    <li>Install Homebrew (if not already installed):
      <pre><code>/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"</code></pre>
    </li>
    <li>Install <code>rbenv</code>:
      <pre><code>brew install rbenv</code></pre>
    </li>
    <li>Initialize <code>rbenv</code>:
      <pre><code>rbenv init</code></pre>
    </li>
    <li>Install Ruby:
      <pre><code>rbenv install 3.2.2
rbenv global 3.2.2</code></pre>
    </li>
  </ol>

  <h3>Linux</h3>
  <ol>
    <li>Install dependencies:
      <pre><code>sudo apt update
sudo apt install git curl libssl-dev libreadline-dev zlib1g-dev autoconf bison build-essential libyaml-dev libreadline-dev libncurses5-dev libffi-dev libgdbm-dev</code></pre>
    </li>
    <li>Install <code>rbenv</code>:
      <pre><code>curl -fsSL https://github.com/rbenv/rbenv-installer/raw/main/bin/rbenv-installer | bash</code></pre>
    </li>
    <li>Add <code>rbenv</code> to your shell:
      <pre><code>echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
source ~/.bashrc</code></pre>
    </li>
    <li>Install Ruby:
      <pre><code>rbenv install 3.2.2
rbenv global 3.2.2</code></pre>
    </li>
  </ol>

  <h3>Windows</h3>
  <ol>
    <li>Download RubyInstaller from <a href="https://rubyinstaller.org/" target="_blank">rubyinstaller.org</a>.</li>
    <li>Run the installer and follow the prompts.</li>
    <li>Check the box to add Ruby to your PATH.</li>
    <li>Install the MSYS2 development toolkit when prompted.</li>
  </ol>

  <h2>2. Install Rails</h2>
  <p>Once Ruby is installed, you can install Rails using the <code>gem</code> package manager.</p>
  <ol>
    <li>Open your terminal or command prompt.</li>
    <li>Run the following command:
      <pre><code>gem install rails</code></pre>
    </li>
    <li>Verify the installation:
      <pre><code>rails --version</code></pre>
    </li>
  </ol>

  <h2>3. Set Up a Database (Optional)</h2>
  <p>Rails uses SQLite by default, but you can configure it to use PostgreSQL, MySQL, or other databases.</p>
  <ul>
    <li><strong>SQLite</strong>: Pre-installed on most systems.</li>
    <li><strong>PostgreSQL</strong>:
      <pre><code>sudo apt install postgresql libpq-dev # Linux
brew install postgresql # macOS</code></pre>
    </li>
    <li><strong>MySQL</strong>:
      <pre><code>sudo apt install mysql-server libmysqlclient-dev # Linux
brew install mysql # macOS</code></pre>
    </li>
  </ul>

  <h2>4. Create a New Rails Application</h2>
  <ol>
    <li>Generate a new Rails app:
      <pre><code>rails new myapp</code></pre>
    </li>
    <li>Navigate to the app directory:
      <pre><code>cd myapp</code></pre>
    </li>
    <li>Start the Rails server:
      <pre><code>rails server</code></pre>
    </li>
    <li>Open your browser and go to <a href="http://localhost:3000" target="_blank">http://localhost:3000</a> to see your new Rails app.</li>
  </ol>

  <h2>5. Troubleshooting</h2>
  <ul>
    <li>If you encounter issues, ensure your Ruby and Rails versions are compatible.</li>
    <li>Check for missing dependencies (e.g., Node.js for the asset pipeline).</li>
    <li>Use <code>bundle install</code> to install required gems for your Rails app.</li>
    <li>If you get any permission error while Rails installation or new project creation like below
    <img src="./images/permission_error.png"/><br/>
    make sure to run again the corresponding step with Admin Privilage
    </li>
  </ul>

  <p>That's it! You now have Ruby on Rails installed and ready to use. Let me know if you need further assistance!</p>
</body>
</html>
