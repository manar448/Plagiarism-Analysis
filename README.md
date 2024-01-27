A checking tool is used to detect code plagiarism of certain assessment. It provides a list of
matching pairs together with the corresponding similarity score (%) of each pair. However,
unfortunately, the same solution can be found in different submissions.
Given a list of submission IDs and a list of matching pairs with their similarity scores (%), it’s
required to calculate the average similarity percentage of the component containing the given
submission ID (i.e. startVertex)

Input:
  • |V| = from 4000 to 8000
  • |E| = sparse or dense
  • # communities = from 1 to 100

Function to Implement
  float AnalyzeMatchingScore(string[] vertices, Tuple<string, string, float>[]
  edges, string startVertex)
  PlagiarismAnalysis.cs includes this method.
  ▪ "vertices": array of submission IDs
  ▪ "edges": array of matching pairs and their similarity score (where Item1: ID1, Item2: ID2,
  Item3: similarity score (%))
  ▪ "startVertex": start vertex to analyze its component
  <returns> average similarity score (%) of each component in the Graph

Example
  vertices1 = { "19T021", "19T024", "19T025"};
  edges1[0] = new Tuple<string, string, float>("19T021", "19T024", 10);
  edges1[1] = new Tuple<string, string, float>("19T024", "19T025", 15);
  startVertex = "19T024"
  expected1 = 12.5;
  vertices3 = { "A1", "A2", "A3", "A4", "A5", "A6" };
  edges3[0] = new Tuple<string, string, float>("A1", "A2", 1);
  edges3[1] = new Tuple<string, string, float>("A2", "A3",2);
  edges3[2] = new Tuple<string, string, float>("A5", "A4",3);
  edges3[3] = new Tuple<string, string, float>("A5", "A6",4);
  edges3[4] = new Tuple<string, string, float>("A3", "A5",5);
  edges3[5] = new Tuple<string, string, float>("A4", "A2",6);
  startVertex = "A6"
  expected3 = 3.5;
