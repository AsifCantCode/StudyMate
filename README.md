<style>
  .fixed-table {
    border-collapse: collapse;
    width: 100%;
  }
  .fixed-table th, .fixed-table td {
    border: 1px solid #ddd;
    padding: 8px;
  }
  .fixed-table .fixed-column {
    position: -webkit-sticky;
    position: sticky;
    left: 0;
    background-color: #000;
    border-right: 2px solid #ddd;
    z-index: 1;
  }
</style>

## Evaluations

<table class="fixed-table">
  <thead>
    <tr>
      <th class="fixed-column">Model</th>
      <th>exact</th>
      <th>f1</th>
      <th>total</th>
      <th>HasAns_exact</th>
      <th>HasAns_f1</th>
      <th>HasAns_total</th>
      <th>NoAns_exact</th>
      <th>NoAns_f1</th>
      <th>NoAns_total</th>
      <th>best_exact</th>
      <th>best_exact_thresh</th>
      <th>best_f1</th>
      <th>best_f1_thresh</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="fixed-column">BanglaBERT_Base_BRQA</td>
      <td>18.95093062605753</td>
      <td>29.891786130011873</td>
      <td>1182</td>
      <td>25.806451612903224</td>
      <td>40.705174200085295</td>
      <td>868</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>314</td>
      <td>26.73434856175973</td>
      <td>0.0</td>
      <td>31.799368113736023</td>
      <td>0.0</td>
    </tr>
    <tr>
      <td class="fixed-column">BanglaBERT_SquadBN</td>
      <td>9.25</td>
      <td>16.132710539947382</td>
      <td>1200</td>
      <td>17.44</td>
      <td>30.654804236698972</td>
      <td>625</td>
      <td>0.34782608695652173</td>
      <td>0.34782608695652173</td>
      <td>575</td>
      <td>47.916666666666664</td>
      <td>0.0</td>
      <td>47.97222222222222</td>
      <td>0.0</td>
    </tr>
    <tr>
      <td class="fixed-column">IndicBERT-BanglaRQA</td>
      <td>10.829103214890017</td>
      <td>24.94270420474983</td>
      <td>1182</td>
      <td>13.940092165898617</td>
      <td>33.159304573749196</td>
      <td>868</td>
      <td>2.229299363057325</td>
      <td>2.229299363057325</td>
      <td>314</td>
      <td>26.56514382402707</td>
      <td>0.0</td>
      <td>27.684840734822945</td>
      <td>0.0</td>
    </tr>
    <tr>
      <td class="fixed-column">IndicBERT-SquadBN</td>
      <td>6.75</td>
      <td>14.464655088919802</td>
      <td>1200</td>
      <td>12.8</td>
      <td>27.61213777072602</td>
      <td>625</td>
      <td>0.17391304347826086</td>
      <td>0.17391304347826086</td>
      <td>575</td>
      <td>47.916666666666664</td>
      <td>0.0</td>
      <td>47.916666666666664</td>
      <td>0.0</td>
    </tr>
    <tr>
      <td class="fixed-column">XLM-Base-RQA</td>
      <td>47.88494077834179</td>
      <td>60.038975495562674</td>
      <td>1182</td>
      <td>64.97695852534562</td>
      <td>81.5277293038653</td>
      <td>868</td>
      <td>0.6369426751592356</td>
      <td>0.6369426751592356</td>
      <td>314</td>
      <td>47.71573604060914</td>
      <td>0.0</td>
      <td>59.86977075782999</td>
      <td>0.0</td>
    </tr>
    <tr>
      <td class="fixed-column">XLM-Base-SquadBN</td>
      <td>23.583333333333332</td>
      <td>31.319512540836108</td>
      <td>1200</td>
      <td>45.28</td>
      <td>60.133464078405325</td>
      <td>625</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>575</td>
      <td>48.0</td>
      <td>0.0</td>
      <td>48.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <td class="fixed-column">mBert-Base-RQA</td>
      <td>46.36209813874788</td>
      <td>58.77937274709887</td>
      <td>1182</td>
      <td>63.133640552995395</td>
      <td>80.04287855653325</td>
      <td>868</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>314</td>
      <td>46.36209813874788</td>
      <td>0.0</td>
      <td>58.77937274709885</td>
      <td>0.0</td>
    </tr>
    <tr>
      <td class="fixed-column">mBert-Base-SquadBN</td>
      <td>25.0</td>
      <td>32.49190584742056</td>
      <td>1200</td>
      <td>46.88</td>
      <td>61.26445922704749</td>
      <td>625</td>
      <td>1.2173913043478262</td>
      <td>1.2173913043478262</td>
      <td>575</td>
      <td>48.0</td>
      <td>0.0</td>
      <td>48.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
