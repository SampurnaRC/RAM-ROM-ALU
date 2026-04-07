#  RAM Design (8-bit)

##  What is RAM?

RAM (Random Access Memory) is used to store data temporarily.
It allows fast read and write operations using an address.

---

##  Single-Port RAM

* One access port
* Can either read or write at a time
* Controlled using write enable (we)

---

##  Dual-Port RAM

* Two access ports
* Can perform read/write simultaneously
* Faster but more complex

---

##  Code Explanation

* Memory is defined as:

  * 256 locations
  * Each stores 8-bit data

* Write operation:

  * Stores input data at given address

* Read operation:

  * Outputs stored data

---

##  Waveform

![RAM Waveform](sim/ram_waveform.png)

---
