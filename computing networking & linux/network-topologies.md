# Network Topologies

A network topology describes how devices and connections are arranged in a network, physically or logically.

## 1. Star Topology
All devices connect to a central device, usually a switch.

**Example:** Computers in a college lab connected to one central switch.

**Advantages:**
- Easy to manage and troubleshoot.
- Failure of one device's link usually affects only that device.

**Disadvantages:**
- Failure of the central switch can disrupt the entire network.
- Requires separate connections to the central device.

## 2. Ring Topology
Devices connect in a circular arrangement, with each device connected to neighboring devices.

**Advantages:**
- Can provide orderly communication in some implementations.
- Some ring designs support alternate paths or fault recovery.

**Disadvantages:**
- A link or device failure can disrupt communication in a simple ring.
- Changes and troubleshooting can be complicated.

## 3. Mesh Topology
Devices connect to multiple other devices. A full mesh connects every device directly to every other device.

**Advantages:**
- Multiple paths can improve resilience.
- A single link failure may not interrupt communication if another route exists.

**Disadvantages:**
- Requires more connections and can be expensive.
- Configuration and management can be complex.

## 4. Bus Topology
All devices share a common main cable called the backbone.

**Advantages:**
- Simple and inexpensive for small, basic setups.
- Requires less cabling than some other designs.

**Disadvantages:**
- Backbone failure can disrupt the network.
- Troubleshooting becomes difficult as the network grows.
- Collisions and performance limitations can occur in traditional shared Ethernet bus networks.

## Quick Comparison

| Topology | Structure | Main Concern |
|---|---|---|
| Star | Central switch or hub | Central device failure |
| Ring | Circular connection | Link or device failure |
| Mesh | Multiple interconnections | Cost and complexity |
| Bus | Shared backbone cable | Backbone failure |

## Cybersecurity Relevance
- Understand which devices and links are critical to network availability.
- Identify single points of failure.
- Plan segmentation and monitoring based on network design.
- Remember that topology alone does not guarantee security.

## Remember
Star = Center, Ring = Circle, Mesh = Multiple paths, Bus = Shared backbone.
