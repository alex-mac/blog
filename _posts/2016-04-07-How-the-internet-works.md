---
layout: post
title:   How the Internet Works
date:   2016-04-07 12:58:00 -0800
---

I recently had the opportunity to interview for an internship position and I was asked a question that I was definitely not prepared for. I don't remember the exact phrasing, but it went along the lines of "Explain what happens when you make a request for a specific website." I knew that this was a fundamental understanding but honestly I have been so occupied with jamming my brain with terminology and trying to learn so many things as fast as possible that I couldn't recall. So, guys and girls, this is going to mark my start in **diving DEEP** rather than *casting my net wide* (learning more in depth rather than learning many things quickly).

Let's get started!

## Intro - Server, Client, Request, HTTP


#### The relationship between Client and Server

A basic concept to understand is the concept of requests and responses. When you type in a URL, you are making a *request* to the internet. The web page that loads is the *response* that you get back. Think of it if you were cheating on an exam (don't!). If you wanted the answer on a particular problem, you would write the question that you need on a piece of paper (or in a text message) and throw it/send it to your friend. The answer that they write on the piece of paper/text is what gets sent back after they process what information you need and after they share their answer with you.

In this example, you are the client. I really don't like the word client because it was so confusing at first. Basically, a client is someone who uses a service (think of it as an *asker* or someone who asks of or for something). If you are going to the dentist, you are a client using the dentist's services (asking to use the dentist's services). If you are hiring a lawyer, you are a client of their services (also asking for access to the lawyer's services). In programming, you can create code to write functions, and you can be a client (someone who uses those premade functions to create your own code). 

In this example, your friend is the server. The server recieves information, and based on the information returns information to the client (the asker, the one who asked for the information).

#### HTTP 

HTTP stands for "Hyper Text Transfer Protocol" and allows for communication between a variety of different computers and supports a ton of different network configurations. To make this possible, it assumes very little about a particular system, and does not keep state between different message exchanges.

In otherwords, HTTP makes it easy for many different computers to talk to each other.

To sum it up, communication between a Client and a Server occurs via a request/response pair. The client initiates an HTTP request message, which is serviced through a HTTP response message in return. 

#### IP Addresses to Domain names

All computers on the internet have a unique numeric address composed of four bytes of data, separated by periods. This is the way computers find "each other" when communicating. 

Of course, it's impractical to remember these specific addresses. That's why we have domain names (ex Google.com). Basically, when you enter a domain name and make a request, that specific domain name is pointed to the server's particular unique address.

| Domain Name  | IP Address    |
|--------------|---------------|
| apple.com    | 17.172.224.47 |
| facebook.com | 31.13.65.1    |
| google.com   | 216.58.192.46 |

when you go to apple.com, your browser asks the DNS server "what is the IP address of apple.com?" The DNS server responds with "17.172.224.47", and the browser can then connect to 17.172.224.47.

In real world terms, it's like how we use street addresses for finding a house, rather than using Latitude and Longitude coordinates.

I know that was a lot of information, but thanks for sticking through it! I learned a lot going over the specifics of how the internet works and still need to cover the specific headers that get sent back, but hope that this intro helps!