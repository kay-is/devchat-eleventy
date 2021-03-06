---
layout: layouts/post.njk
title: >
  158 iPS Internet of Things (IoT) with Olivier Bloch
date: 2016-06-23 07:00:55
episode_number: 158
duration: 48:20
audio_url: https://media.devchat.tv/iphreaks/iPS158OlivierBloch.mp3
podcast: iphreaks
tags:
  - iphreaks
  - podcast
---

This episode was recorded live from The [Microsoft Build Conference](https://build.microsoft.com/) 2016. In this episode we chatted with [Olivier Bloch](https://twitter.com/obloch) of the [Microsoft Azure IoT](https://www.microsoft.com/en-us/cloud-platform/internet-of-things) team about the [Internet of Things](https://en.wikipedia.org/wiki/Internet_of_things) and the [Azure IoT Suite](https://www.microsoft.com/en-us/cloud-platform/internet-of-things-azure-iot-suite). &nbsp;Resources

- [azure/azure-iot-sdks](https://github.com/azure/azure-iot-sdks)
- [ms-iot/samples](https://github.com/ms-iot/samples)
- [Microsoft Azure IoT Starter Kits](https://azure.microsoft.com/en-us/develop/iot/starter-kits/)
  &nbsp;Picks
- [Sous Vide](https://en.wikipedia.org/wiki/Sous-vide) (Olivier)

### Transcript

**_[This episode is sponsored by Hired.com. Every week on Hired, they run an auction where over a thousand tech companies in San Francisco, New York and L.A. bid on iOS developers, providing them with salary and equity upfront. The average iOS developer gets an average of 5-15 introductory offers and an average salary offer of $130,000/year. Users can either accept an offer and go right into interviewing with a company or deny them without any continuing obligations. It’s totally free for users, and when you're hired they also give you a $1,000 signing bonus as a thank you for using them. But if you use the iPhreaks link, you’ll get a $2,000 bonus instead. Finally, if you're not looking for a job but know someone who is, you can refer them on Hired and get a $1,337 bonus as thanks after the job. Go sign up at Hired.com/iphreaks]_**

**JAIM:** Hey everybody and welcome to the iPhreaks Show! Today on our panel, we have Andrew Madsen.

**ANDREW:** Hello from Microsoft BUILD at San Francisco.

**JAIM:** And I’m Jaim Zuber, also from Microsoft BUILD in San Francisco. Today in our show, we’ve got Olivier Bloch.

**OLIVIER:** Hi guys.

**JAIM:** Want to tell us a little bit about yourself?

**OLIVIER:** Yeah, definitely. So I’m a French guy who came to the US eight years ago, working for Microsoft. These days, I’m a program manager in the Azure IoT Team, engineering team. So working on SDKs for developers and developer experience in that field that I’m passionate about, so the internal things area.

**JAIM:** Cool. It’s like we’re playing buzzword bingo as [inaudible] whiz. [Inaudible] It’s a big word and everyone thinks they know what it means. Hey just mean tiny devices and a [inaudible] I had to reboot.

**OLIVIER:** Actually, the interesting thing about the internal thing is that everyone talks about the things because that’s the visible part of the iceberg. But IT is about – way more than just that; it’s actually about what’s going to happen with all these sensor’s data that’s been generated and pushed up in the Cloud or some gateway to something and how are you going to analyze all that. Are you going to be smart about reacting to all that data? Are you also going to trigger commands back to the devices? How are you going to manage these devices?

So it includes so many different topics that are just – they go beyond having a smart [inaudible] that tells you one, to refill the milk. It’s pretty interesting. Everyone I’ve been talking to at the event at BUILD here has different scenarios. People came with super interesting stories and scenarios and ideas that we didn’t even think were existing or in someone’s mind so that it’s pretty interesting.

So think about – in the past, we used to call that machine to machine or embedded or connected stuff, smart devices. But now it goes from just the devices to much more in the Cloud. You can imagine whatever crazy scenarios you want and our services will help you implement that.

**ANDREW:** What part of this whole internet of thing ecosystem does Azure IoT provide?

**OLIVIER:** Yeah, so Azure IoT is several things; it’s a series of services around Azure that allow you to go from ingesting data from devices that you can authenticate in your service and you can manage from the service to what we call the Azure IoT Suite which is the bundle of pre-configured services that is some sort of a turnkey solution for you to deploy on your subscription of use. We have a couple of these which are the remote monitoring one and predictive maintenance one so the names are pretty explicit.

Just after a few clicks, what you’re going to deploy with that is a series of these services that will do everything from getting the data from devices. In the remote monitoring example, we get humidity and temperature data from whatever type of devices. Being able to monitor that data, being able to set up rules to trigger events based on specific events, on happenings on that data, you’re able also to look into a line of business applications to trigger these actions based on something happening on devices.

So think about Azure IoT as this offering that is built at the same time a box of Lego blocks that you can aggregate and build your own stuff or as a pre-configured set of solutions that you can just install and start using and eventually customize your own needs.

**ANDREW:** Everything you’ve talked about just now is about taking data from an IoT device, pushing it up to the Cloud and being able to do [inaudible] you’ve talked about. What about when you need to go the other way?

**OLIVIER:** The Azure IoT Hub service which is that [inaudible] for devices, allows you to do both. So the devices are uniquely identifying themselves to the service and the service knows which device it is coming from and allows for an application which is running in Cloud or in the device to send a command back to that device. So that communication is bi-directional using Azure IoT Hub and uses the same communication channel, meaning that the device could be on, waiting for a command, and from the Cloud, you’re going to send these commands. That’s pretty neat and kind of unique because of their bi-directionality actually is not something that is very common out there in terms of the various services available for IoT Cloud services.

**ANDREW:** So for background – we’re iOS developers, our listeners are iOS developers. I also have a background as a hardware engineer. So this intersection between hardware and software and pervasive networking [crosstalk] with mobile is all really interesting to me. I’m curious to know, say I’m a hardware engineer and I’m working on an IoT device, I want to use Azure IoT, how do I get started? What’s the first step?

**OLIVIER:** So you have to roll things to look into. The first step is definitely to look into our developer’s center that actually you can find on ak.mf.azureiotdev. This dev center will link you to the resources you can look at.

We do have a couple of things as a hardware [inaudible] that you might be interested in. At BUILD, we just announced the availability of a series of hardware kits. We call it Starter Kits for Azure IoT and it had various type of hardware that are ready to go to being connected to Azure IT. So you write your code whether in Node, C – whatever you want for these devices, using the usual tools that makers or the hardware engineers are using like Arduino IDE or others from your Mac, from whatever. Once you have connected those devices, you can start implementing some intelligence up there in the Cloud. For that, you can use a usual SDK that you use for tinkering those Azure services.

Now to your iOS scenarios, if you want to have – I’m thinking about a typical IoT home automation scenario, you want to have a controller on your iOS device or you want your iOS device to actually share the data of the various [inaudible] devices and centers it can connect to using Bluetooth or other things like that to Azure IoT Hub.

We just published on Monday a new portable class library so that you can build Xamarin application for your iOS device that will be able to connect to IoT Hub. So your iOS device will act as a gateway for all these [inaudible] that it might not be directly connected to the internet to participate in an IT solution that’s broader. That might be a good place to start with. Looking into our Azure IoT SDKs, in particular, looking into the [inaudible] library that we have in the C# - like in the C# SDK. And look at the samples we have there as well for you to get started rapidly.

**JAIM:** For Xamarin, that’s the C#-based development. For iOS, we talked of [crosstalk] – Miguel de Icaza earlier today but this would be going out a week or two before. So any plans for Native?

**OLIVIER:** There are plans for Native. As of right now, the core of our developer SDK for connecting devices o Azure IoT Hub is the C-based code. So we actually target micro-controllers for that but obviously, it’s pretty straightforward to make that C code run in the context of Xcode and to use it on iOS devices.

We’ve now productized a [inaudible] that you have internally, the [inaudible] stats which basically is just instructions set to tell you how to do that but we definitely plan to have that published on the Azure IoT SDK’s repo. Obviously, someone is faster than us to publish that. We welcome all the pull requests and contributions from the community because it’s something important to us that we are conscious that there are like so many of these platforms out there that needs to be addressed. We need to be open in terms of not just publishing our code to try and address these [inaudible] platforms but also accepting that all the [inaudible] would tackle and contribute their own implementation of our SDKs on these platforms were not covered yet.

**ANDREW:** So how much of the Azure IoT system is open source?

**OLIVIER:** Right now [crosstalk].

**ANDREW:** Or which part?

**OLIVIER:** Only SDKs are open source, fully open source meaning that those are the ones that you use to configure the service and send message from the [inaudible] to the device and the SDKs that runs on the device to connect to [inaudible] as device clients. All these are fully open source.

The service itself that run on Azure and the code and its implementation is not open source. This is something we’re looking into, whether we should or not. Right now, there’s not a demand for that because what people care about is the code that runs on their devices or in their applications and solutions on web apps that interact with the service so we definitely want to focus on that.

The idea here is actually to provide a lot of flexibility and choices. These SDKs, when it comes to the service client SDKs, we have support for Java, JavaScript, C#. On the device side of things, we have C as I’ve mentioned; we have JavaScript, we have Java, we have C#, we have Python. We do have support – native support for iOS and [inaudible] in addition to the PCF-Xamarin library that we mentioned already.

So we do want to be native for mobile platforms that are out there including iOS. We do think that our C code base, which is already available, will be what we’re going to build on to do that.

**JAIM:** So what’s the process for wiring this into your app? Say we’re doing Xamarin [inaudible] SDK, what’s the interface like? What is the typical thing you’d be doing? [Crosstalk]

**OLIVIER:** So typically the – yeah, the various operations you’re going to do are first [inaudible] creates the instance of the service. So step number one, you need to have an Azure IoT Hub deployed on your IoT subscription to be able to connect things to it. So then when we look at the Azure IoT SDK’s repo, you’re going to find a bunch of samples. These samples are about connecting the device, sending data and receiving commands back from the Cloud. It’s pretty straightforward using the SDKs because there is a command which is create the client which establishes the secure connection to the service. Then you open the message layer defining what protocol you want to use, whether it’s HTTP, NTP or [inaudible] and the nest operation is to send, to [inaudible] to message.

You can – basically, we have a role messaging infrastructure so you send whatever you want. If you want to serialize your data in a JSON message or something else, do whatever you want. Send those messages; we manage for you within the SDK, only [inaudible] making sure that you receive it on a notification when a message is well-received and so on so all that is part of the SDK. So basically you have one function to [inaudible] which is send message async.

**JAIM:** So if you’re in a hurry, you don’t want to do Xamarin and you want to do it now, is there a REST API that [crosstalk] you can use?

**OLIVIER:** You can definitely leverage REST APIs for interacting with the Azure IoT Hub. That [inaudible], the messaging communication is established over whether NTP or HTTP REST as well but that’s not the preferred one or MQTT. Because the messaging of the device [crosstalk].

**JAIM:** I know some of those acronyms but our [crosstalk].

**ANDREW:** Oh yeah – those letters?

**OLIVIER:** Okay, so NTP and MQTT are [inaudible] machine protocols. They basically are protocols that allow you to have the machines talking to each other and all the protocol of [inaudible] bi-directionality and so it’s taken care of by these protocols. They’re [inaudible] a standard of the industry today that lots of very smart guys are participating in discussion and writing. Basically, we complied to these standards of these industry for communicating across two machines. So we implemented that in our service, in the Cloud and in our SDKs so that you can have that used there.

The reason why we’re using these machine to machine protocols is because the HTTP REST has limitations. The typical limitation is that you don’t have bi-directionality. If you’re [inaudible] and you want to receive a command from the Cloud, you have to [inaudible] for messages. This is not very efficient when you are in the IoT space. You’d buy [inaudible] device that runs on the battery and that gets connected only once a day to send its [inaudible] data to be pulling every minute to get a commit.

These machine to machine protocol, they are very much optimized to not use to much of the bandwidth and the engine when they have this connection open and they have to keep alive handshaking happening. That means you can run on a battery powered device and have these devices being always connected and receive a command and acts in an instant they receive a command or the instance have been emitted in the Cloud. This is why we would tell them about these various protocols that are available.

**JAIM:** Definitely. One thing is that you realize what IoT is, how it’s actually being used – HTTP has just been the default for development for years. You’re getting to – [inaudible] you’re talking about you might have a device out in the middle of nowhere which is calling in to a cellphone signal or satellite. [Crosstalk]

**OLIVIER:** Exactly.

**JAIM:** All the overhead from your HTTP request doesn’t make sense. I always knew protocols that do cool things.

**OLIVIER:** Exactly. You definitely described the exact scenario it tackles which represents a huge portion of the IoT devices out there because very often, when you think – when these [inaudible] IoT, we see the big, nice, shiny [inaudible] object. What we don’t see as a consumer is all these other devices that represent billions that all the press analyst talk about that are the IoT devices out there. These are things as simple as temperature sensor which is a remote farm somewhere or on a cattle.

**JAIM:** All these [inaudible] for things that are for like how much grain you have in your silo? [Crosstalk]

**OLIVIER:** Exactly. There are already a lot of these devices out there today but they’re not connected to a Cloud. They might be connected to a local gateway or to a local application and what we want to offer is the possibility to actually extend the capabilities of these solutions because farmers today, they do modern farming. They have all these – I’m not saying that’s a good example, we can continue talking about these ones which is like you have all these sensors that allow you to measure some silos, measure cattle. And they have applications or run on a PC or whatever and that they gather the data and do limited [inaudible] reports or not.

So what we want to offer is the possibility to extend a solution to something that’s going to go broader not only for this farmer to be able to benefit from very high [inaudible] and storage and so on from the Cloud but also eventually for companies to build solutions that it will send to farmers as certain software service solution that run in Cloud. Say, “Hey, instead of having all these [inaudible] installed and this applications run, you install these sensors, you install that black box gateway and then the only thing that it have to do is go to a portal on the web, log in and then you’re going to have all the information about your cattle’s [inaudible]. We’re going to connect you to your peers or connect you to other professionals, or we connect you to the provider to the food of your animals. We’re going to connect you to all the rest of your industry so that you can actually focus on what is your job which is farming versus trying to install that fricking software on that PC.

So this is exactly what it is about which is allowing to extend these existing solution where devices are connected and share the information and data to broader solutions that get more data [inaudible], deal with more information [inaudible]. That’s really about it.

**JAIM:** So if you’re creating all this data, what’s the management story like? [Inaudible] Most of our audience, they’re mobile developers so what’s on the client side? We are not doing a ton of work on the server stuff but what – it’s for you to say I’ve created some smart [inaudible] switch. What type of data are you getting on the server?

**OLIVIER:** It totally depends on the solution you want to implement. The light switches – there’s like two [inaudible] I would see there. The one is a use of that light switch which were – you want to optimize on energy consumption and you want to eventually optimize in comfort as in you send a voice command and it’s going to command the light switch or dimmer to go down or something like that. The second one is the [inaudible] of your system, especially if you want to actually – maintaining like for example, [inaudible] light switch but it might not be for consumer. It could be for an enterprise, for a warehouse, something like that. So you want might to eventually know when bulbs are running out in a warehouse if you’re the company selling these bulbs because like the Home Depot of the world, they don’t go change the bulbs themselves. They have a company doing that for them.

As that company, you might want to have a way to have remote [inaudible] of these systems and infrastructures because you don’t want to have a guy going through all the Home Depots of the world and then we visualize all the bulbs that are running out or what not. So you want to have that type of data.

The first type of data are things that you’re going to deal on what we call the [inaudible] path of the plan. Solutions which is you’re going to react on the stream of data. You might not need to store it somewhere; it’s just that you apply filters on these stream of data and you immediately trigger an action.

For example you [crosstalk].

**JAIM:** What do the filters look like? Is this in code [crosstalk]?

**OLIVIER:** The filter will be – yeah, for filtering this kind of data, you have various types of services. One is called extreme analytics where you define what an input is which is IoT Hub which is the device gateway, the [inaudible] in the Cloud through that thing. Then you have some of these [inaudible] that can look at that stream of data and you use SQL type of queries in code to say, “Hey, [inaudible] – that type of data goes over that threshold, then publish and alert.”

Then what you would do is you would have a [inaudible] or web app or something code that actually reacts on that specific alert. So this is what I would call the hot path. The data’s coming in and immediately, you do something.

The cold pat is a place where you gather lots of data and you [inaudible] that in some data [inaudible], in some big data solution [inaudible] or not. After the data’s been logged with tons of information, metadata, [inaudible] that coming from what time did he come in, what level of alerts, warning, information it is and so forth. All of that is managed using the regular data mining tools or what not. You produce dashboards to reporting to do deep analytics, machine learning analytics and so forth on the backend. These are the two path for the data in the IoT solution, IoT scenarios that actually we need to think about.

**JAIM:** How do you create the dashboard? Is it point and click? Are you actually coding up HTML or – what’s the experience like?

**OLIVIER:** Instead of creating a dashboard for visualizing and starting playing with the data. So when it comes to Azure IoT, we have what you call the Azure IoT Suite where in a couple of clicks, you can deploy these pre-configured solutions we’re talking about. One is remote monitoring, the other one is predictive maintenance and we’re going to add more soon.

The idea that you create your subscription on Azure, if you don’t have one, then you go to azureiotsuite.com and create a new solution, click on remote monitoring. It’s going to take five to ten minutes to deploy all those services in the subscription that will have everything from the device plugin, which is IoT Hub, to a website and uses [inaudible] controls to see graphs and meters and so on. We have a starting point for building your own dashboard. That’s one way of doing it, or you have an already type of scenario that we address in the IoT suite in mind.

The second way of doing and actually to leverage [inaudible] available here and there. [Inaudible] a great tool for doing dashboards and you can ingest data from data sets that you push data into from IoT Hub. You can definitely say “Hey, I’m going to have [inaudible] ingested. I’m going to push that to data sets – [inaudible] data sets, then in my [inaudible] portal, we would say, “Ah, from that data set, I would be interested in that type of data. I want to show it as a graph, as a table or what not until you build – you dynamically build that dashboard of yours and then you can create what we call the reports. They are actually that you can then share with your employees, customers or what not so that you can have access to that data and eventually have control over it.

**ANDREW:** Tell us some of the things that people are actually using Azure IoT for.

**OLIVIER:** So it’s a – huge amount of things. So you’ve heard – if you listen to the BUILD Keynote that BMW is offering Cloud services around the use of the car and so on, they’re based on Azure IoT solutions. We’re working with companies like ThyssenKrupp who are doing elevators and doing all the maintenance of their elevators using Azure IoT, optimizing on their calls and on their efficiency, thanks to all the [inaudible] that you can have from the Cloud.

It goes also into home automation type scenarios or into smartwear. It’s pretty broad in terms of what it’s used for. We did focus on the initial automation as the first type of scenario we want to tackle. Our services do that really well but they also fit it for a bunch of things that even in ourselves, we don’t even think of.

So we have a very interesting discussion with a guy early on the booth who has a system which is about using light bulbs and sending a specific frequency that your eye doesn’t see through the light to delocalized objects or people or things in the room or in the building. So you have these various lamps that send a specific frequency, each of them and from the device you wear or the device that’s on-board, you’ll be able to triangulate where you are based on these frequencies because you know where the lightbulbs are, right? Basically, they’ll use sonar systems and then what they do is basically offer building mappings and real time localization of instrument, tools, people and just based on the lightbulbs that are up there.

Those are the scenarios that are totally crazy because they are basically matching – it’s hard to figure out the [crosstalk]. Imagine in this huge building we are in, all the lights could be sonar systems that are actually editing their own frequency. The device you’re wearing detects them, receives that frequency and they will say, “Okay, I’m assuming that [inaudible] to the signal so that means I’m at that distance of that point.” Then I’m receiving that other frequency and that trend would mean something that that distance of that second point and third point, you can know exactly where you are based on that. Then this device will communicate to Azure IoT and be able to report to the IT solution exactly where it is.

So when you’re in a building, you have GPS signal and the accuracy of a GPS signal is not as good as that because I’m trying [inaudible] now can be at the centimeter. So you can delocalize in a place based on that. Any object that actually is equipped with that receptor for these frequencies.

**JAIM:** That’s pretty cool.

**OLIVIER:** That’s a pretty cool system, right?

**JAIM:** Most of the internal triangulation approaches has not worked as well like iBeacons.

**OLIVIER:** Yeah.

**JAIM:** Because when you’re inside, they’re bouncing everywhere. Bluetooth is really hard to get.

**ANDREW:** That’s the nice thing about light; it does bounce around but it does not have nearly the difficult propagation characteristics of radio like Bluetooth.

**OLIVIER:** Exactly. I don’t remember the name of the company but yeah, I think they’re on to something here.

**ANDREW:** Yeah, that’s cool. You talked a little bit about home automation. That’s something that I think a lot of – some of the stuff we’ve talked about here is really cool and transformative but it’s for industries that the average person never thinks about. Most people don’t – are not farmers. They don’t think about how [crosstalk] farmers run. Everybody lives somewhere and has a house and so I think home automation is one of the first things people think about when they think of [inaudible] things.

Apple has a system for home automation called HomeKit which is nothing – is really nothing about what you’re talking about with Azure. But as iOS developers, we know that we can create a HomeKit device and there are really nice APIs on iOS to talk to that stuff. Do you do anything [inaudible]?

**OLIVIER:** Yeah, so here’s the way I see that. I think HomeKit is great and is really very much optimized for home automations so they will also be applied in building automation, the more [inaudible] version of home automation. I like it. We’re not in the business of – as the Azure IoT team, in the business of building something that does exactly that but I would love for publishing a sample or something they will allow you guys to connect a HomeKit system up to Azure IoT and access the power of Azure.

When I say the power of Azure, there’s all the big data, all the storage, all the machine learning they can think of. That means that once you have your data come from these devices up there and once you’re able to actually go back and control these devices from that backend, off you go. I don’t see that as being something totally unthinkable and impossible; we actually do want to do that as in interact with another Cloud that does IoT or another solution that does the IoT.

You’re mentioning automation but I want to go back to another sample which is very interesting which is Sigfox. Sigfox is a company that does that IoT network of theirs that allows for devices like very low consumption and don’t run all the time to be connected. So they have their own series of antennas that cover lots of Europe that’s starting to be deployed in the US so they have their own infrastructure of antennas. You have a device that is Sigfox enabled. It could be whatever. It could be a home automation device. You don’t even need to have an installation in your place; as long as your house is covered by the range of the antennas which they use past frequencies that have a very long range, you just have a device that is Sigfox enabled and immediately, it contributes to a scenario which is an IoT scenario.

Think about your smart thermostats. This one, if it’s connected using Sigfox, you can as a developer or as a consumer to actually see the data coming into the Sigfox Cloud but that cloud only – it allows you to have device connected sending data and eventually receiving commands. It doesn’t do anything else. But leveraging the power of Azure by connecting this Sigfox Cloud into ours, that means you can do way more. You can apply smarts with AI using machine learning. You can apply dashboarding, you can do all that. You can eventually build a solution where you actually offer to your various customers as service on top of that data.

When it comes to automation, the first scenarios I think of is energy savings. Lights, as a consumer, what you might want to do is actually have information about how you’re doing in terms of energy consumption, how you’re doing compared to your neighbors, how you’re doing in general which is what [inaudible] does a lot but eventually inject different type of information or there’s a bad weather coming. Eventually, my system would need to crank up a little bit of temperature because a bad weather’s coming or I know that in the morning, there’s going to be better weather so I should eventually turn down the temperature to save energy in any ways, as soon as the sun comes out, it’s going to heat up and I don’t need to heat up my house. So these kind of things because you would have your solution connected to a broader set of solution and services. Thanks to something like Azure, you’ll be able to do more. As a company, you’ll be able to offer more type of services to the customers.

So when I think about home automation and HomeKits and Google Weave and things like that, I totally think that it does make sense for us to have these easily connectible to Azure IoT, to the Azure IoT Hub so that you guys can develop solutions and leverage all the smarts, all the storage and so forth they [inaudible] in the Cloud.

**JAIM:** Yeah, definitely. We’re app developers, we’re not honestly going out [inaudible] servers or could do clusters of tons of data,

**OLIVIER:** That’s the thing that scares you. [Chuckles]

**ANDREW:** Yeah, absolutely. If I have [inaudible] so, right?

**OLIVIER:** Coming from the embedded device [inaudible] upload side of things, my background is in developing the things that go in your car in your hard [inaudible] timed systems like robot arm controllers and things like that.

The first time I was offered to join the Azure IoT team was like “Whoa, what’s that?” I was happy enough because they offered me a job like talking to device developers. So I’m comfortable with that however, the more I work with what we have in the backend, the more I’m just like, “Okay, so we’re talking about interacting with a service versus interacting with an OS. That felt so different; it has an API service that you as a developer just tackle. It gives me services like an OS platform gives you. Not the same type of services but still, you’re requesting information, giving information, you send a control – pretty much the same principles, right? The good news is that to develop for this Cloud, especially for Azure, we can do it on your Mac using your favorite language because we have SDKs for pretty much everything out there.

So as a developer, you should start looking into these end to end scenarios because they’re not so scary and they’re not so hard to implement. If you want to implement a simple weather station for example, of your own, go get one of the starter kits that is like hardware. You can tinker that, connect temperature, humidity, whatever sensor’s on it. Gather the data, whether you want it to go through your iOS device as a gateway to the Cloud, whether it’s directly connected, your choice, then you can very rapidly following some of the instructions in these end to end samples create an IoT Hub to ingest the data.

You say, “Okay, so in my logic, I want to get that data, eventually apply some filters to trigger alert. So I have two things to go there; one is called the Azure [inaudible] that were some streams of data and another is called Azure Functions. Azure Functions is an event-driven trigger so basically, it’s something you code. You don’t have to deal about [inaudible] to VM or to website [inaudible] there were not. You just go to the portal for Azure, you say create new function. You decide what is going to be triggered on, whether it’s going to be an HTTP REST API so from somewhere else, you can call that API and it will trigger the action. Whether it’s an event hub which is that stream of service that when you receive data, filters license or something. Whether it’s a blob storage which is something we store a file that has data in there.

Azure Functions, you will use – for now, there’s Node and C# code you can put in the portal. You don’t need a developer tool or what not; you just drop the code up there and this thing will be executed when it’s triggered. So if you define that as the HTTP trigger when something, whether it’s a device or another service, will call that REST API, that code will be executed in the Cloud. But what’s happening in the back as a VM deployed with the code, we don’t have to care. It’s all taken care of for you.

From there, you have a system that ingest the temperature data, eventually filters the data and then does something like sending a command back to the device for setting the temperature for example, or sends a tweet or sends an email to your device or an SMS because you want to be notified when you’re [inaudible] is on. Eventually, you want to say, “Hey, I want to turn my heat off from my phone” because that’s one of the common scenarios and you would say, “Async command triggers the action for the function, the function talks back to the device through IoT Hub and boom, you set the temperature remotely.

Few services very straightforward and I’m sure any of the smart [inaudible] that you guys are, in about 20 minutes, you have that deployed.

**ANDREW:** You said this earlier but you’re making it sound like snapping Lego together.

**OLIVIER:** Sorry, again?

**ANDREW:** You make it sound like snapping Lego together.

**OLIVIER:** Yeah it is. That’s exactly what it is about. It’s actually snapping these boxes with lots of Legos, that’s what it turns out to be. It’s way simpler, we think. Actually, we’re working a lot on providing tools that will allow you to actually not have to deal with all the deployment and maintenance and so forth of these services. So when you think about the cloud offerings, it goes from what we call infrastructure as a service where basically it’s like – think of like bunch of servers that are hosted and maintained by us that you run your stuff. Then you have the platform as a service which is more advanced type of service where you have APIs that you can use to do something. Then you have the software as a service that does beyond where actually you want to implement a scenario and it’s already pre-baked for you.

So we’re not there yet when it comes to IoT but with the IoT Suite, we’re getting there. We’re [inaudible] to that but you as a developer, then you can look at the various levels. Depending on what you want to do, what you can do, what you know how to do, you can go for one another. If you want to do it yourself and build your own VMs and just publish them and have them do all the work, well go [inaudible]. If you want to go advance services that do a bunch of things for you, you just aggregate lots of Legos, you go with the past offering. If you’re the guy who just wants to basically leverage a service like device [inaudible] for example from us, go for the SaaS offering.

**JAIM:** So you talked about connecting with the Cloud, communicating with the Cloud back to the device.

**OLIVIER:** Yeah.

**JAIM:** How do you handle cases where you internet goes down? Maybe the WiFi’s up, you’re internet’s down. Is that handled [inaudible] direct connection with your [inaudible]?

**OLIVIER:** So this is a very common scenario where a device is not permanently connected. So we do handle in our SDKs the fact that the device is not permanently connected. So when the application will come back to online where we establish a connection, if you have a set of messages that have been bufferized in between, they’re going to be sent. So this is definitely an infrastructure that we provide in our SDKs so that you don’t have to think about it.

From there, you also have to be conscious of what’s going on, what you develop for the device like when you develop an application on an iOS device, you have to consider the fact that the device might not be always connected. You switch to airplane mode or something like that so in your application, you actually benefit from the OS infrastructure that is going to give you notifications like “hey, I went off” or things like that in your application. It’s pretty much the same thing from the SDK’s perspective for IoT Hub which I should be able to [inaudible] kid of bufferization and send as bulk and so forth. We handle the communication establishments and retries and so on for you. This is something that’s definitely top of our minds when we implement these SDKs for developers.

**ANDREW:** I want to hear more about the starter kits you mentioned. So you have some hardware starter kits. I think one of them was mentioned on stage at the Keynote yesterday where you’ve got some – I don’t know if you’ve [inaudible] but you’ve got some native [inaudible] stuff.

**OLIVIER:** Yes, so we basically have several kits from [inaudible] and others and so now we just have five and we’re going to have plenty more. The idea of these kits is to have a collection of different types of devices. It goes from the micro controllers that you program with C as in the Arduino IDE up to Intel Edison board which runs the Octo which is a Linux distribution or Raspberry Pi that can run both Windows IoT Core or Raspbian or other Raspberry Pi OS.

So we have that range of different types of devices that are available in the form of kits. In terms of price ranges then, we are around the hundred dollars price points while you have the board and the set of [inaudible] plus we have instructions for you to follow that will help you to do two things – one is use the Azure IoT Suite so you can very rapidly deploy a full remote monitoring solution that will monitor temperature and humidity from these devices. You’ll see a real time charge, you’ll be able to define rules on this dashboard. You’ll be able to be notified and so forth and extend that solution to your needs.

The second one is what we call a DIY scenario where you actually manually deploy an IoT Hub and a couple of other services on Azure to do a very slight – very simple temperature anomaly detections system where you would [inaudible] temperature, you want to define its threshold and you’re going to trigger an action from the services.

**ANDREW:** So you actually showed that on stage yesterday. For our listeners who probably didn’t see it, they had a board with temperature sensor and they guy hit it with a can of freeze spray and it dropped down to I don’t know what but got really cold and then that triggered an event that made his shirt light up [crosstalk]. None of us knew that his shirt had lights in it so it was a fun little demo.

**OLIVIER:** Cool.

**ANDREW:** Sounds like that start – the hardware he used to do that is actually available as a startup [crosstalk] minus the shirt. I don’t think it comes with the shirt.

**OLIVIER:** Exactly, so the shirt actually they would build because I was actually leading the development of that demo and had some very cool devs in my team that actually did the whole hardware part of it using the kit. The way [inaudible] actually, we used the Adafruit Feather M0 WiFi kit which is a really tiny microcontroller using WiFi. And what we did actually, we just went to some Home Depot shop and bought some LEDs of 12-volts – some stripes of [inaudible] LEDs. And we had our – actually our GPM or [inaudible] guy was like super geeky and so on, he went out and created this boards of cardboards where he laid all the LEDs and we actually blacked out the LEDs we don’t want to be visible.

**ANDREW:** Okay,

**OLIVIER:** We made it like – super like – you know, it’s a maker thing. So then what would happen is it’s just an on and off trigger. We don’t actually [crosstalk].

**ANDREW:** Controlling each of the LEDs, right?

**OLIVIER:** We could do that, it would’ve taken more time so [inaudible] just on and off. So the little board is connected to a little relay, a 12-watt relay and just like, say, on off on that relay and that relay actually turned on the LEDs. So that little device was connected over WiFi and was receiving a command from Azure IoT Hub.

So our solution was about – we had this other device with the temperature [inaudible] connected to that same IoT Hub. We were receiving the temperature information. In the back, we had an Azure function monitoring for alerts on that temperature. When that threshold went over – below 20 degrees, it was actually calling a command to the device IoT Hub to the [inaudible] devices unto another device to the shirt to trigger the lights.

I demoed that as well yesterday during my session that you can see on Channel 9 if you want to check it out and showed all the things end to end, the various function and the services [inaudible] deployed, the architect of that solution. It was pretty fun to deploy and really it’s significant in terms of what it says. You have a device sending data to Azure, Azure doing some processing and sending command to another device. The two specific device actually because we’re able to uniquely identify all of these devices. That was a pretty fun demo to do.

**ANDREW:** It was a fun demo.

**OLIVIER:** And yeah, the [inaudible] are looking pretty good. I’m happy with that. [Chuckles]

**ANDREW:** Yeah, it was up my alley. You were talking a little bit about these starter kit and you mentioned Raspberry Pi. I already know what your answer’s going to be but I’ve been having fun playing around with Swift which you can now write and compile Swift for Raspberry Pi. So when are you going to do a Swift SDK?

**OLIVIER:** I want it to be supported for sure. [Crosstalk] I think it’s definitely important for our device client SDK to support Swift so that’s definitely something that – I have several discussions here about [inaudible] and so on. We just called [inaudible] – in terms of supporting devices and platforms, we went first for the embedded devices. We went first for supporting embedded Linux, microcontrollers and so on. So [inaudible] was mentioning our core SDK is a C-based SDK but now we are actually sending that to other types of devices including mobile devices.

So the PCL–Xamarin library was a low hanging fruit, boom, it’s there. Now we need to look closer into not only other [inaudible] like Swift or Objective-C – I might say that you guys prefer Swift these days but having a way for you to develop natively for that.

I don’t think it’s going to be too much of a problem to actually have our C stack being exposed in a Swift API set so definitely something I want to tackle. [Crosstalk]

**ANDREW:** Yeah, in general, Swift does really well with calling C – with wrapping a C API [crosstalk]. Swift and C [inaudible] really well.

**OLIVIER:** Yeah, and by the way if you have [inaudible] to where you get started with that, [inaudible] I can go back to my dev team and tell them, “Hey, I prototyped that guys, now it’s up to you to prototype that.” [Chuckles]

So actually, there’s one question for you guys because you’re in that area [inaudible] which is how do you see something like the Apple Watch entering into a scenario like that? When you see something like an application that would connect any way through the phone and the phone itself, you have Swift support or whatever, could actually make that watch participate in IoT solution easily?

**ANDREW:** Yeah.

**OLIVIER:** It’s something it would do, right? So that’s definitely the type of samples that I want to implement as well because why not, it’s totally doable.

**ANDREW:** I think that would be a great sample because for example, one of my favorite things about my Apple Watch, and I think everybody would say this, is the way it does notifications. So if I can get a notification that my garage door opened because my wife just got home or whatever – this is home automation stuff again but – yeah, absolutely.

**OLIVIER:** Yeah, and I think it would be pretty straightforward to implement that as soon as you can develop that iOS app that actually will communicate with your home or with that garage open or what not, you don’t.

**ANDREW:** Yeah.

**OLIVIER:** And the use of Azure IoT Hub in there would definitely help you in various ways as in like having notification up even if your device is not connected to be able to notify you as soon as it gets back online or these kind of things, so that’s definitely something that could be done very easily. Once again using Xamarin today but in the near future, using Swift or Objective-C so that’s definitely something we want to implement. That’s a pretty cool scenario in mind.

I do that with my [inaudible] day where the band actually have – the [inaudible] that we did with the shirt. On the Keynote, you didn’t see it all because some of it is being cut [inaudible] but basically what it had is as I presented my session, I had a customized version of the remote monitoring not taking temperature immediately from a device but taking heart beat and skin temperature from my band, from my phone. And what Dana was doing also was tuning in to some Twitter information, some Twitter account with hashtag into the same portal and it was measuring both. The goal- I focused on Twitter only but when I could’ve done really easily is I started doing squats to see my heart beat going up and trigger that alert that would’ve lit up the shirt.

That initial demo – wanted to do is [inaudible] didn’t want to do the squat on stage but definitely this kind of scenario’s what you include in this wearable devices into an IoT scenario [inaudible] in terms of notification but also to me in terms of the sensors because it gives a lot of information.

I have a UV center in here that actually could be very useful in lots of cases to contribute that information to something that would be crowd sourced for informing people, “Hey, bring your sound screen because on that beach is like UV level is super high.” The information is coming from people wearing these bands that have a UV sensor on top and that contribute information up to some Cloud, crowd source solution that I could be definitely – these kind of things you can do with these wearables that go beyond just notifications.

**JAIM:** Yeah, very cool.

**ANDREW:** I didn’t know it had a UV sensor. That’s fun.

**OLIVIER:** Yeah, it’s pretty cool. It does a lot of things. [Chuckles]

**ANDREW:** If our listeners want to know more and maybe play around with this, what are the best resources for them to go?

**OLIVIER:** The two places that we recommend for you guys to go, the first one is our GitHub repo for our SDKs. That’s kind of raw but I’d like to send developers down there.

**ANDREW:** If I could read somebody’s source code, I feel like I’d get a lot better idea of how to hold [inaudible].

**OLIVIER:** So basically go to github.com/azure/azure-iot-sdks.

**ANDREW:** We’ll put a link in our show notes.

**OLIVIER:** And then the second place you might want to go is actually our samples page on Azure, a.k.a. ms/azureiotsamples. In there you have [inaudible] samples including the ones that powered Starter Kits that we have. So we’re going to grow – you’re going to find maybe a dozen samples up there but we would grow that list and obviously, we accept contributions as well here so if you have great ideas, you can go there. These would be the two places I will send developers.

**ANDREW:** You mentioned you did a session on all this.

**OLIVIER:** Yeah.

**ANDREW:** It’s my understanding that the session and videos for this are [crosstalk].

**OLIVIER:** They’re online, yeah. I think mine is B844; that’s the name was Developer’s Introduction to Azure IoT.

**ANDREW:** Okay. What if you want to buy a starter kit?

**OLIVIER:** What if you want to buy a starter kit? So you go to – I’m going to add the URL as well to the starter kit – azrure.com/iotstarterkit. I think that’s the one and this is where you see all the kits and all the links for getting started, for buying them and [inaudible].

**ANDREW:** Cool.

**JAIM:** Anything else you want to say before we get to the picks?

**OLIVIER:** Well, thanks for having me here. It was interesting. Definitely want to continue the engagement with you guys and iOS developers because I think there’s much we can do there. Let’s meet on GitHub, on the [inaudible]. You can find me on Twitter as well, @obloch and let’s continue a discussion.

**JAIM:** Cool. Thanks Olivier.

**OLIVIER:** Thank you guys.

**ANDREW:** So we’re not doing picks for the hosts because we’re all out of picks at the show but Olivier, do you have a pick?

**OLIVIER:** Yes, I have a small pick for my [inaudible] these days in San Francisco. I had my first sous-vide cooked [inaudible]. Lots of you might have already; it was my first one. It was perfectly cooked and as a big geek [inaudible], my first thing going back would be to go buy a sous-vide machine to do my cooking. That was my cherry pick of the week, I guess.

**ANDREW:** Are you going to hook your sous-vide machine up to Azure Internet of Things?

**OLIVIER:** Well you know, anything is possible. [Chuckles]

**ANDREW:** Why not!

**OLIVIER:** I might go crazy. Actually, [crosstalk] turning on the sous-vide machine like when I’m leaving the office before coming back home, that would be great, yeah.

**JAIM:** Totally.

**ANDREW:** Alright, thanks again.

**OLIVIER:** Thank you guys.

**_[Bandwidth for this segment is provided by CacheFly, the world’s fastest CDN. Deliver your content fast with CacheFly. Visit cachefly.com to learn more]_**
