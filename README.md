# COMP3027-3927-A3-Algorithm-Design
# VX: csprojhelp 备注: github
# COMP3027/3927-A3 专业辅导

“Historical” background. It is a well-known and historically established fact that
Viking engineers had ingenious networks to distribute their (non-alcoholic) ale to
the Vikings.1 Unfortunately, a new chief has come to power and he’s rather set on
making sure he gets all the ale and as fast as possible using the existing network.
Even more unfortunately, you’re the second in command, so it’s your job to handle
that. So, you grudgingly closed off everyone else’s access to this delicious drink,
leaving only the chief’s tap functioning. For a time this was good, but the chief
thinks he isn’t getting his ale fast enough, so you’re instructed to investigate the
current network and its associated flow of ale and determine whether this can be
improved, possibly by modifying the network. You’d better do this fast, he seems
thirsty!
Throughout this assignment, you can assume that the network you’re given is
connected, that the capacities are all positive integers, and that the flow you’re given
is feasible and integtal. Additionally, you can assume that you’re given the network
and the flow’s residual graph in adjacency list form.
Problem 1. (20 points)
We start by investigating whether the current amount of ale reaching the chief
is really the best we can do given our current network. To allow for future use of
our methods, instead of checking only the current network and flow of ale, your
aim is to design an algorithm that can determine this for any network and flow. In
other words, given a directed graph G and two vertices s (the brewery: the source!)
and t (the chief’s house, unfortunately the terminus) along with capacities of all the
pipes in our network, as well as the current flow through these pipes, design an
algorithm to determine whether the current flow is the maximum possible in the
network.
Your task is to design the above algorithm. Your algorithm should run in O(n +
m) time, where n is the number of vertices and m is the number of edges of the
network.
a) Describe the algorithm in plain English.
b) Prove its correctness.
c) Establish its time complexity

Problem 2. (80 points) (COMP3027 only)
Time to explore the capabilities of our network. We first want to determine
whether there are any pipes that are crucial to the flow of ale. We call a pipe
expandable if increasing its capacity by 1 increases the value of the maximum flow
by 1 as well. Analogously, we call a pipe limiting if reducing its capacity by 1
decreases the value of the maximum flow by 1 as well. We start by figuring out
whether every network actually has these types of pipes.
Does every network have at least one expandable pipe? Prove your answer is
correct, i.e., prove that every network has such an edge, or provide a network
that doesn’t and explain why.
a)
Does every network have at least one limiting pipe? Prove your answer is
correct, i.e., prove that every network has such an edge, or provide a network
that doesn’t and explain why.
b)
Next, it’s time to design an algorithm to actually find the expandable pipes and
make our chief happy. Design an algorithm that given a directed graph G and two
vertices s (the brewery) and t (the chief’s house) along with capacities of all the
pipes in our network, as well as a maximum flow through these pipes, returns all
expandable pipes.
Your task is to design the above algorithm. Your algorithm should run in O(m)
time, where m is the number of edges of the network.
c) Describe the algorithm in plain English.
d) Prove its correctness.
e) Establish its time complexity.
Expanding these pipes doesn’t seem what the chief had in mind. He wanted a
complete overhaul of the entire network to maximize the throughput to his house by
redistributing the capacity of the pipes in the network (you can move capacity from
any pipe to any other pipe, no restrictions as long as the capacities stay integer).
Your goal in doing so is to see if there’s any way at all to facilitate the chief’s
demand for a total throughput (maximum flow) of at least k.
Your task is to design an algorithm that given a directed graph G and two
vertices s (the brewery) and t (the chief’s house) along with capacities of all the
pipes in our network, as well as a maximum flow through these pipes, returns
whether the capacities can be redistributed in such a way to allow for a maximum
flow of k. Your algorithm should run in O(m) time (i.e., not depend on k and k is
not a constant), where m is the number of edges of the network.
f) Describe the algorithm in plain English.
g) Prove its correctness.
h) Establish its time complexity

Problem 3. (80 points) (COMP3927 only)
Time to explore the capabilities of our network. We first want to determine
whether there are any pipes that are crucial to the flow of ale. We call a pipe
expandable if increasing its capacity by 1 increases the value of the maximum flow
by 1 as well. Analogously, we call a pipe limiting if reducing its capacity by 1
decreases the value of the maximum flow by 1 as well. We start by figuring out
whether every network actually has these types of pipes.
Does every network have at least one expandable pipe? Prove your answer is
correct, i.e., prove that every network has such an edge, or provide a network
that doesn’t and explain why.
a)
Does every network have at least one limiting pipe? Prove your answer is
correct, i.e., prove that every network has such an edge, or provide a network
that doesn’t and explain why.
b)
Next, it’s time to design an algorithm to actually find the expandable edges and
make our chief happy. Design an algorithm that given a directed graph G and two
vertices s (the brewery) and t (the chief’s house) along with capacities of all the
pipes in our network, as well as a maximum flow through these pipes, returns all
expandable pipes.
Your task is to design the above algorithm. Your algorithm should run in O(m)
time, where m is the number of edges of the network.
c) Describe the algorithm in plain English.
d) Prove its correctness.
e) Establish its time complexity.
A rebellion is brewing2
, as the other Vikings are rather unhappy about their lack
of ale. The rebels have also come to you with a request: design an algorithm to find
all limiting pipes in the network, so they can leverage this when going to the chief.
Your task is to design an algorithm that given a directed graph G and two
vertices s (the brewery) and t (the chief’s house) along with capacities of all the
pipes in our network, as well as a maximum flow through these pipes, returns all
limiting pipes. Your algorithm should run in O(n · m) time, where n is the number
of vertices and m is the number of edges of the network.
f) Describe the algorithm in plain English.
g) Prove its correctness.
h) Establish its time complexity
