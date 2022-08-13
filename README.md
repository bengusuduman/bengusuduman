- 👋 Hi, I’m @bengusuduman
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
bengusuduman/bengusuduman is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

//6. video 24.dk kadar
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class GameManager : MonoBehaviour

{
    public GameObject DogmaNoktasi;
    public GameObject VarisNoktasi;
    public int AnlikKarakterSayisi=1;
    public List<GameObject> Karakterler;

   
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.A))
           foreach (var item in Karakterler)
            { 
                if (!item.activeInHierarchy)
                {
                    item.transform.position = DogmaNoktasi.transform.position;
                    item.SetActive(true);
                    AnlikKarakterSayisi++;
                    break;
                }
            }

    }
    public void AdamYonetimi(string veri, Transform Pozisyon)
    {
        switch (veri)
        {
            case "x2":
                int sayi = 0;
                foreach (var item in Karakterler)
                {
                    //0   5
                    //1
                    //2
                    //3
                    //4

                    if(sayi < AnlikKarakterSayisi)
                    {
                        if (!item.activeInHierarchy)
                        {
                            item.transform.position = DogmaNoktasi.transform.position;
                            item.SetActive(true);
                            AnlikKarakterSayisi++;
                            
                        }
                        else
                        {
                            sayi = 0;
                            break;
                        }

                    }


                   
                }


                   break;





        }








    }




}
