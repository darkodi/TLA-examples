We’ll have an idealized model of sending messages when the receiver
doesn’t automatically accept them. Maybe the receiver is a friend who’s going in and out
of cell coverage. We can approximate this with a two-turn cycle:

1. On the sender’s turn, they put a message in transit.
2. On the receiver’s turn, they either receive a message in transit or
do nothing (they’re outside cell coverage).

While we have a definite order on how the messages are sent and an order in which
they are received, they aren’t ordered while in transit. The receiver can get the messages
in transit in any order. This means we have two sequences for to_send and received, but
a set for in_transit.