---
title: "[dart&flutter] List<String>,ListView"
categories: 
  - dart
  - flutter
  - dart class
tags: 
  - flutter
  - dart
toc: false
toc_sticky: false

---

<iframe width="100%" height="800" src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/42bb0efd-ac37-4c2f-b9c4-1e6519aac45e/%E1%84%92%E1%85%AA%E1%84%86%E1%85%A7%E1%86%AB_%E1%84%80%E1%85%B5%E1%84%85%E1%85%A9%E1%86%A8_2021-10-26_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_7.42.40.mov?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20211109%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20211109T182847Z&X-Amz-Expires=86400&X-Amz-Signature=c760658c632d7cbcd51c81647bd957870926faf00de1a1a5343b2b94cc1e5f60&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22%25E1%2584%2592%25E1%2585%25AA%25E1%2584%2586%25E1%2585%25A7%25E1%2586%25AB%2520%25E1%2584%2580%25E1%2585%25B5%25E1%2584%2585%25E1%2585%25A9%25E1%2586%25A8%25202021-10-26%2520%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE%25207.42.40.mov%22" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

```dart
import 'package:flutter/foundation.dart';
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

// MyApp is a StatefulWidget. This allows updating the state of the
// widget when an item is removed.
class MyApp extends StatefulWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  MyAppState createState() {
    return MyAppState();
  }
}

class MyAppState extends State<MyApp> {
  final List<String> items = [
    '신사와 아가씨',
    '빨강 구두',
    '국가대표 와이프',
    '원 더 우먼',
    '홍천기',
    '검은태양',
    '두 번째 남편',
    '연모',
    '달리와 감자탕',
    '원 더 우먼(재방송)',
    '홍천기(재방송)',
    '신사와 아가씨(재방송)',
    '두 번째 남편(재방송)',
    '연모(재방송)',
    'KBS 네트워크 특선',
    '국가대표 와이프(재방송)',
    '드라마스페셜2021-시네마회수',
    '달리와 감자탕(재방송)',
    '검은태양(재방송)',
    '빨강 구두(스페셜)',
  ];

  @override
  Widget build(BuildContext context) {
    const title = '드라마 대본 20선';

    return MaterialApp(
      title: title,
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: Scaffold(
        appBar: AppBar(
          title: const Text(title),
        ),
        body: ListView.builder(
          itemCount: items.length,
          itemBuilder: (context, index) {
            final item = items[index];
            return Dismissible(
              // Each Dismissible must contain a Key. Keys allow Flutter to
              // uniquely identify widgets.
              key: Key(item),
              // Provide a function that tells the app
              // what to do after an item has been swiped away.
              onDismissed: (direction) {
                // Remove the item from the data source.
                setState(() {
                  items.removeAt(index);
                });

                // Then show a snackbar.
                ScaffoldMessenger.of(context)
                    .showSnackBar(SnackBar(content: Text('$item dismissed')));
              },
              // Show a red background as the item is swiped away.
              background: Container(color: Colors.red),
              child: ListTile(
                title: Text(item),
              ),
            );
          },
        ),
      ),
    );
  }
}
```

<iframe width="100%" height="800" src="https://www.youtube.com/embed/iEMgjrfuc58" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
