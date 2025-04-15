using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class EnemyMove : MonoBehaviour
{
    public float speed = 6f;
    public Transform[] checkpoints;
    private int checkpointId = 0;
    float step;

    void Start()
    {
        step = speed * Time.deltaTime;
    }

    void Update()
    {
        if (checkpointId < checkpoints.Length)
        {
            Transform currentCheckpoint = checkpoints[checkpointId];

            transform.position = Vector3.MoveTowards(transform.position, currentCheckpoint.position, step);

            if (Vector3.Distance(transform.position, currentCheckpoint.position) < 0.25f)
            {
                checkpointId++;
            }
        }
        else
        {
            checkpointId = checkpoints.Length;
        }
    }
}
