# Flutter-UI-Helper
"Flutter UI Helper" repository contains CODE snippet of various widgets. The purpose is to help developers with the source code so that they can build a UI quickly and easily. 

## FloatingActionButton

### Default Size
```dart
 FloatingActionButton( 
   onPressed: () {}, 
   child: Icon(Icons.arrow_back),
   shape: CircleBorder(),
   backgroundColor: Colors.grey,
 )
 ```
### Mini Size
 FloatingActionButton( 
   onPressed: () {}, 
   mini: true, 
   child: Icon(Icons.arrow_back),
   shape: CircleBorder(),
   backgroundColor: Colors.grey,
 )


## Horizontal ListView Builder (5 container)

``` dart
Container(
              width: double.infinity,
              child: ListView.builder(
                  scrollDirection: Axis.horizontal,
                  itemCount: 5,
                  itemBuilder: (context, index) {
                    return Row(
                      crossAxisAlignment: CrossAxisAlignment.start,
                      children: [
                        Padding(
                          padding: const EdgeInsets.only(left: 10.0, top: 10),
                          child: Container(
                            margin: EdgeInsets.only(right: 16),
                            height: 200,
                            width: 200,
                            decoration: BoxDecoration(
                                borderRadius: BorderRadius.circular(10),
                                // color: index % 2 == 0 ? Colors.amber : Colors.blue,
                                color: Color.fromARGB(255, 155, 183, 250)),
                          ),
                        ),
                      ],
                    );
                  }),
            ),
```

## Card (a text and a image in a column)

```dart
 Container(
                      height: 150,
                      width: 150,
                      child: Card(
                        elevation: 8,
                        shape: RoundedRectangleBorder(
                          borderRadius: BorderRadius.circular(10.0),
                        ),
                        color: Colors.white,
                        child: Padding(
                          padding: const EdgeInsets.all(10.0),
                          child: Column(
                            mainAxisSize: MainAxisSize.min,
                            children: [
                              Expanded(
                                flex: 1,
                                child: Text(
                                  "In Progress",
                                  style: TextStyle(fontWeight: FontWeight.bold),
                                ),
                              ),
                              Expanded(
                                flex: 4,
                                child: Image.asset(
                                  "images/rising.png",
                                  fit: BoxFit.cover,
                                ),
                              )
                            ],
                          ),
                        ),
                      ),
                    )
```
