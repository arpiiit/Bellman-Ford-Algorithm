# Bellman-Ford-Algorithm

//Bellman ford Algorithm
//import java.lang.*;
//
//class Graph {
//    class Edge {
//        int src, dest, weight;// source destination and weight
//
//        Edge() {
//            src = dest = weight = 0;// create a new ege and initilize zero
//        }
//    }
//
//    ;
//    int V, E;
//    Edge edge[];
//
//    Graph(int v, int e) {
//        V = v;
//        E = e;
//        edge = new Edge[e];
//        for (int i = 0; i < e; ++i)
//            edge[i] = new Edge();
//    }
//
//    void Bellman(Graph graph, int src) {
//        int V = graph.V;
//        int E = graph.E;
//        int dist[] = new int[V];
//
//        for (int i = 0; i < V; ++i)
//            dist[i] = Integer.MAX_VALUE;
//        dist[src] = 0;
//
//        for (int i = 1; i < V; ++i) {
//            for (int j = 0; j < E; ++j) {
//                int u = graph.edge[j].src;            //case 1
//                int v = graph.edge[j].dest;
//                int weight = graph.edge[j].weight;
//
//                if (dist[u] != Integer.MAX_VALUE && dist[u] + weight < dist[v])
//                    dist[v] = dist[u] + weight;
//            }
//        }
//        for (int j = 0; j < E; ++j) {
//            int u = graph.edge[j].src;
//            int v = graph.edge[j].dest;           // same as case 1
//            int weight = graph.edge[j].weight;
//
//            if (dist[u] != Integer.MAX_VALUE && dist[u] + weight < dist[v]) {
//                System.out.println("Graph contain negatuve graph cycle");
//                return;
//            }
//        }
//        printArr(dist, V);
//    }
//
//    private void printArr(int dist[], int V) {
//        System.out.println("Vertex distance from source");
//        for (int i = 0; i < V; ++i)
//            System.out.println(i + "\t\t" + dist[i]);
//
//    }
//
//    public static void main(String[] args) {
//        int V=5;
//        int E=8;
//        Graph graph=new Graph(V,E);
//    }
//
//
//}
