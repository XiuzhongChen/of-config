bin_PROGRAMS=ofc-server ofc-agent
ofc_server_SOURCES=common.c common.h comm.h server_ops.h server_ops.c server.c netconf-server-transapi.c ofconfig-transapi.c ofconfig-datastore.c data.h ovs-data.c
ofc_server_LDADD=@OVS_LIBS@
ofc_agent_SOURCES=common.c common.h comm.h agent.c

# according to condition, add needed source codes
if dbus
ofc_server_SOURCES+=comm_dbus.h server_comm_dbus.c
ofc_agent_SOURCES+=comm_dbus.h agent_comm_dbus.c
else
ofc_server_SOURCES+=comm_socket.h comm_socket.c server_comm_socket.c
ofc_agent_SOURCES+=comm_socket.h comm_socket.c agent_comm_socket.c
endif

# list of all conditional sources (because of packaging)
EXTRA_DIST=comm_dbus.h server_comm_dbus.c agent_comm_dbus.c comm_socket.h comm_socket.c server_comm_socket.c agent_comm_socket.c edit-config.c

