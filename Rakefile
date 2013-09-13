require 'rakeup'

RakeUp::ServerTask.new do |t|
  t.port = 8558
  t.pid_file = 'tmp/server.pid'

  t.run_command = "thin -P #{t.pid_file} -p #{t.port} start --daemonize"
  t.start_command = "thin -P #{t.pid_file} -p #{t.port} start -D --daemonize"
  t.stop_command = "thin -P #{t.pid_file} -p #{t.port} stop"
  t.restart_command = "thin -P #{t.pid_file} -p #{t.port} restart"
end
