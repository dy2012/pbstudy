all: proto_addressbook write_message read_message

proto_addressbook:
	protoc --cpp_out=. addressbook.proto

write_message: write_message.cc addressbook.pb.cc
	g++ write_message.cc addressbook.pb.cc -L/usr/local/lib -lprotobuf -lprofiler -o write_message

read_message: read_message.cc addressbook.pb.cc
	g++ read_message.cc addressbook.pb.cc -L/usr/local/lib -lprotobuf -o read_message

clean:
	rm -f write_message read_message addressbook.pb.cc addressbook.pb.h 
