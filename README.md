**Game Technologies Lab**\
**Jiayu Yan**\
**2D Automatically-generate-scenes in Unity 3D**

**Proposal**

TThis project is an attempt to study how to create 2D maps randomly.

**Reserach**

Compared to the complex 3D scene design, the 2D scene design is more simple because it is flat. The 3D scene is more dependent on the model, and most of the 2D scenes are created by the image material. The sprite function in unity should be used here。


**Porcess**

1. Insert a 2D image material, then click the sprite editor on the right to edit it

2. In the "sprite editor" panel, click on the slice, the image material will be automatically split, click apply.

3. Create an empty GameObject. Add the sprite renderer component.

4. Create a new script file, attach it to the Main Camera, double-click to open the script and add a set of sprites that declare map elements and elements
```
public GameObject floor;
```
```
public Sprite[] floorSp;
```

5. Then return to the main interface, drag the sprite to the floorsp.

6. Retun to the script and add:

```
for(int i=0;i<10;i++){
```
```
for(int j=0;j<10;j++){
```
```
GameObject floor0= (GameObject)Instantiate(floor,new Vector3(0.32f*i,0.32f*j,0),Quaternion.identity);
```
```
floor.GetComponent<SpriteRenderer>().sprite=floorSp[Random.Range(0,floorSp.Length-1)];
}
```

**Project**

Randomly generate maps each time

**citation**

https://docs.unity3d.com/ScriptReference/SpriteRenderer.html\
https://docs.unity3d.com/ScriptReference/Sprite.html

