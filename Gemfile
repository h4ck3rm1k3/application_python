#
# Copyright 2015, Noah Kantrowitz
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
ENV["LOAD_PATH"] = File.join(
  File.dirname(__FILE__),
  '../rubygems/lib')


def dev_gem(name, path: File.join('..', name), github: nil)
  path = File.expand_path(File.join('..', path), __FILE__)
  if File.exist?(path)
    puts "adding #{name} and #{path}"
    gem name, path: path
  elsif github
    puts "adding #{name} and #{github}"
    gem name, github: github
  else
    # see https://github.com/poise/application_python/pull/63
    #gem name
    #raise "missing #{name}"
  end

end

#dev_gem 'rubygems', github: 'rubygems/rubygems'
#, path: ''
dev_gem 'halite', path: '../halite-2'
dev_gem 'berkshelf', path: '../berkshelf'
source 'https://rubygems.org/'

gemspec path: File.expand_path('..', __FILE__)


dev_gem 'poise', github: 'poise/poise'
dev_gem 'poise-application', path: '../application', github: 'poise/application'
dev_gem 'poise-application-git', path: '../application_git', github: 'poise/application_git'
dev_gem 'poise-boiler', path: '../poise-boiler'
dev_gem 'poise-languages', github: 'poise/poise-languages', path: '../poise-languages'
dev_gem 'poise-python', path: '../poise-python', github: 'poise/poise-python'
dev_gem 'poise-service', github: 'poise/poise-service',path: '../poise-service'
