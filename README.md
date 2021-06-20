using UnityEngine;
using System.Collections;

public class ScoreShadow : MonoBehaviour
{
	public GameObject guiCopy;		// Uma cópia da partitura.



	void Awake()
	{
		// Defina a posição ligeiramente para baixo e atrás do outro gui.
		Vector3 behindPos = transform.position;
		behindPos = new Vector3(guiCopy.transform.position.x, guiCopy.transform.position.y-0.005f, guiCopy.transform.position.z-1);
		transform.position = behindPos;
	}


	void Update ()
	{
		// Defina o texto para ser igual ao texto da cópia.
		GetComponent<GUIText>().text = guiCopy.GetComponent<GUIText>().text;
	}
}
