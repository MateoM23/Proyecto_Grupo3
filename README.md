// ignore_for_file: deprecated_member_use

import 'dart:html';

import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
  const MyApp({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      title: 'MyApp',
      home: MiPagina(),
    );
  }
}

class MiPagina extends StatelessWidget {
  const MiPagina({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Widget Scaffold'),
      ),
      body: Center(
        child: Align(
          alignment: Alignment.topRight,
          child: FlatButton(
            padding: const EdgeInsets.symmetric(horizontal: 60, vertical: 13.0),
            color: Colors.lightBlue,
            child: const Text(
              "Generar",
              style: TextStyle(fontSize: 18.0, fontWeight: FontWeight.bold),
            ),
            onPressed: () {Navigator.push(context,
    MaterialPageRoute(builder: (context) => const Segunda()),
  ); },
          ),
        ),
      ),
    );
  }
}

class Segunda extends StatelessWidget{
  const Segunda({Key? key}) : super(key: key);

  @override 
  Widget build (BuildContext context){
    return Scaffold(
      appBar: AppBar(
        title: const Text('Imagen Aleatoria'),
      ),
      body: Center(
        child: Row(
        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
      children: [
          Image.network('https://picsum.photos/250?image=9'),
          Image.network('https://picsum.photos/250?image=4'),
        ], 
        ),
      ),
      );
  }
}
