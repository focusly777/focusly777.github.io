---
title: "[flutter&dart] Drawer"
categories: 
  - dart
  - flutter
  - dart class
tags: 
  - flutter
  - dart
  - drawer
toc: true
toc_sticky: true
comments: true

---

<iframe width="100%" height="900" src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/4cca0966-e571-4dcb-85b8-cdea1f5f94ce/%E1%84%92%E1%85%AA%E1%84%86%E1%85%A7%E1%86%AB_%E1%84%80%E1%85%B5%E1%84%85%E1%85%A9%E1%86%A8_2021-10-26_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_4.12.07.mov?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20211109%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20211109T183754Z&X-Amz-Expires=86400&X-Amz-Signature=42e57d43b3986361738df98b3c3820aaf31f000eb2fa97f9f4ca71026dde589d&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22%25E1%2584%2592%25E1%2585%25AA%25E1%2584%2586%25E1%2585%25A7%25E1%2586%25AB%2520%25E1%2584%2580%25E1%2585%25B5%25E1%2584%2585%25E1%2585%25A9%25E1%2586%25A8%25202021-10-26%2520%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE%25204.12.07.mov%22" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

```dart
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  static const appTitle = '유주의 인생맛집순위';

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      title: appTitle,
      home: MyHomePage(title: appTitle),
    );
  }
}

class MyHomePage extends StatelessWidget {
  const MyHomePage({Key? key, required this.title}) : super(key: key);

  final String title;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text(title)),
//appbar
      body: const Center(
        child: Text('My Page!')
//text,
      )
//body(center),
      drawer: Drawer(
        // Add a ListView to the drawer. This ensures the user can scroll
        // through the options in the drawer if there isn't enough vertical
        // space to fit everything.
        child: ListView(
          // Important: Remove any padding from the ListView.
          padding: EdgeInsets.zero,
          children: [
            const DrawerHeader(
              decoration: BoxDecoration(
                color: Colors.blue,
              ),
              child: Text('통계'),
            ),
            ListTile(
              title: const Text('암기할것'),
              onTap: () {
                // Update the state of the app
                // ...
                // Then close the drawer
                Navigator.pop(context);
              },
            ),
            ListTile(
              title: const Text('암기중'),
              onTap: () {
                // Update the state of the app
                // ...
                // Then close the drawer
                Navigator.pop(context);
              },
            ),
            ListTile(
              title: const Text('암기완료'),
              onTap: () {
                // Update the state of the app
                // ...
                // Then close the drawer
                Navigator.pop(context);
              },
            ),
          ],
        ),
      ),
    );
  }
}
```