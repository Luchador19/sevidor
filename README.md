# sevidor
Servidor
using UnityEngine;

public class PlayerVision : MonoBehaviour
{
    public float visionRange = 5f;
    public LayerMask targetLayer;

    void Update()
    {
        RaycastHit hit;
        if (Physics.Raycast(transform.position, transform.forward, out hit, visionRange, targetLayer))
        {
            Debug.Log("Se detectó un objeto: " + hit.collider.name);
        }
    }
}
