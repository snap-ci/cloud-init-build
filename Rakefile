require 'rake/clean'

desc "generate cloud-init rpm"
task :default do
  pwd = Dir.pwd
  sh("wget 'ftp://ftp.redhat.com/pub/redhat/linux/enterprise/6Server/en/RH-COMMON/SRPMS/cloud-init-*'")

  Dir["cloud-init-*.rpm"].each do |rpm|
    rm_rf("#{pwd}/jailed-root")
    sh(%Q{rpmbuild --rebuild #{rpm} --buildroot #{pwd}/jailed-root  --define "_topdir #{pwd}" --define "_rpmdir #{pwd}"})
    mkdir_p 'pkg'
    mv Dir['noarch/*.rpm'].first, 'pkg'
  end
end
