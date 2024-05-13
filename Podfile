# Podfile
platform :ios, '14.0'
use_frameworks!
inhibit_all_warnings!

source 'https://github.com/CocoaPods/Specs.git'
source 'https://github.com/exmg/livery-sdk-ios-podspec.git'

target 'livery-sdk-ios-example' do
  pod "Livery", "3.0.0"
end

post_install do |installer|
  installer.generated_projects.each do |project|
    project.targets.each do |target|
      if ['Kronos', 'lottie-ios', 'Sentry'].include? target.name
        target.build_configurations.each do |config|
          config.build_settings['BUILD_LIBRARY_FOR_DISTRIBUTION'] = 'YES'
        end
      end
    end
  end
end
