
guard :shell do
  watch %r{^docs/.*adoc} do |m|
    `rake asciidoc:create`
  end
end

