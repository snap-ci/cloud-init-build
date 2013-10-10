require 'rake/clean'

desc "generate cloud-init rpm"
task :default do
  pwd = Dir.pwd
  sh("wget 'ftp://ftp.redhat.com/pub/redhat/linux/enterprise/6Server/en/RH-COMMON/SRPMS/cloud-init-*'")
  sh(%Q{rpmbuild --rebuild cloud-init-*.rpm --buildroot #{pwd}/jailed-root  --define "_topdir #{pwd}" --define "_rpmdir #{pwd}"})
  mkdir_p 'pkg'
  mv Dir['noarch/*.rpm'].first, 'pkg'
end
