# Bash Crawl personal notes

I=coins,diamonds,sword,amulet,

HP=15

```mermaid
---
config:
  theme: redux
---
flowchart TD
 subgraph s1["Vault"]
        G_2{{"glass(requires ice shards)"}}
        H["stronghold"]
        G_1>"scroll"]
  end
 subgraph s2["Cellar"]
        B_1>"scroll"]
        B_2{{"treasure(amulet)"}}
        C["armoury"]
  end
 subgraph s3["Armoury"]
        D["chamber"]
        C_1>"scroll"]
        C_2{{"potion(<br>y--&gt;+5(HP=15) <br>n--&gt;+10(HP=10)<br>)"}}
        C_3{{"treasure(sword)"}}
  end
 subgraph s4["Entrance"]
        B["cellar"]
        G["vault"]
        A_1>"scroll"]
  end
 subgraph s5["Chamber"]
        E_1>"scroll"]
        E_2{{"treasure(coins | diamonds)"}}
        E_3@{ label: "spell('ln')" }
        E_4{{"statue(-5HP)"}}
        E_4_1{{"pieces"}}
        E["portal"]
  end
 subgraph s6["Portal"]
        F["library"]
        E_5{{"monster"}}
  end
 subgraph s7["Library"]
        F_1{{"tome"}}
        F_2>"scroll"]
  end
 subgraph s8["Tome Contents "]
        F_1_1(("1.ls color upgrade"))
        F_1_2(("2.pushd, dirs, popd"))
        F_1_3(("3.simple brace expansion and for loops"))
        F_1_4(("4.emacs"))
        F_1_5(("5.tmux terminal multiplexer"))
        F_1_6(("6.tree"))
  end
    start(["bashcrawl"]) --> A["entrance"]
    A ---> B & G
    A --> A_1
    B ---> C
    B --> B_1 & B_2
    C ---> D
    C --> C_1 & C_2 & C_3
    D --> E_1 & E_2 & E_3 & E_4
    E_4 --> E_4_1
    D ---> E
    E ---> F
    E --> E_5
    F --> F_1 & F_2
    F_1 --> F_1_1 & F_1_2 & F_1_3 & F_1_4 & F_1_5 & F_1_6
    G --> G_1 & G_2 & H
    E_3@{ shape: hexagon}
```
