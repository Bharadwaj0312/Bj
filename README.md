import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('Row Widget Layout Example'),
        ),
        body: Center(
          child: Row(
            mainAxisAlignment: MainAxisAlignment.spaceAround, // Space evenly between children
            crossAxisAlignment: CrossAxisAlignment.center, // Center children vertically
            children: <Widget>[
              Column(
                mainAxisAlignment: MainAxisAlignment.center,
                children: <Widget>[
                  Icon(Icons.home, size: 50, color: Colors.blue),
                  SizedBox(height: 8), // Space between icon and text
                  Text('Home'),
                ],
              ),
              Column(
                mainAxisAlignment: MainAxisAlignment.center,
                children: <Widget>[
                  Icon(Icons.search, size: 50, color: Colors.green),
                  SizedBox(height: 8),
                  Text('Search'),
                ],
              ),
              Column(
                mainAxisAlignment: MainAxisAlignment.center,
                children: <Widget>[
                  Icon(Icons.settings, size: 50, color: Colors.red),
                  SizedBox(height: 8),
                  Text('Settings'),
                ],
              ),
            ],
          ),
        ),
      ),
    );
  }
}

