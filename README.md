# test
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class SCR_MoveAB_bidi : MonoBehaviour {

    public Transform sphereTransform;
    public float direction = 1f;

    void Update () {
        moveBetweenAB();		
    }

    public void moveBetweenAB()
    {
        if (Mathf.Abs(sphereTransform.position.x) >= 4.50f) direction *= -1f;
        sphereTransform.Translate(0.05f * direction,0,0);
    }
}
