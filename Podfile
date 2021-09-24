# Podfile
platform :ios, '12.0'
use_frameworks!
inhibit_all_warnings!

source 'https://github.com/CocoaPods/Specs.git'
source 'https://github.com/exmg/livery-sdk-ios-podspec.git'

target 'livery-sdk-ios-example' do
  pod "Livery", "1.2.4"
  
  post_install do |installer|
    installer.pods_project.build_configuration_list.build_configurations.each do |configuration|
      configuration.build_settings['ARCHS'] = 'arm64'
    end
  end
end
