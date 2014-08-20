Amonitoe
========
class Millepied < ActiveRecord::Base
  has_many_remote :legs, :path => "/millepieds/:id/legs"
end

m = Millepied.new
m.id   # => 1
m.legs # => Requests "/millepieds/1/legs"
