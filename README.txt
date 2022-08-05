took a while for postgres to work, had error messages about postgres role not found, wtf?

had to manually set the password in the console via k8s

awx-manage resetpassword admin

or something like that

history:

  kubectl config get-contexts
 2079  kubectl apply -f https://raw.githubusercontent.com/ansible/awx-operator/0.26.0/deploy/awx-operator.yaml
 2080  curl -s "https://raw.githubusercontent.com/kubernetes-sigs/kustomize/master/hack/install_kustomize.sh"  | bash
 2081  ls
 2082  vi awxinstallviakustomize.yaml
 2083  kustomize build .
 2084  ./kustomize build .
 2085  mv awxinstallviakustomize.yaml kustomization.yaml
 2086  ./kustomize build .
 2087  ./kustomize build . > viakustomize.yaml
 2088  vi viakustomize.yaml
 2089  kubectl apply -f viakustomize.yaml -n awxtesting
 2090  kubectl get pods -n awx
 2091  kubectl get pods -n awxtesting
 2092  ls -lrt
 2093  vi viakustomize.yaml
 2094  grep image: viakustomize.yaml
 2095  vi viakustomize.yaml
 2096  kubectl apply -f viakustomize.yaml -n awxtesting
 2097  kubectl get pods -n awxtesting
 2098  cat /usr/local/bin/generateapassword
 2099  ls -lrt
 2100  vi awxdeployment.yaml
 2101  mv awxdeployment.yaml awx-demo.yaml
 2102  vi kustomiz
 2103  vi kustomization.yaml
 2104  kustomize build . > viakustomizewithawxdeployment.yaml
 2105  ./kustomize build . > viakustomizewithawxdeployment.yaml
 2106  vi viakustomizewithawxdeployment.yaml
 2107  grep -ri ingress
 2108  vi viakustomizewithawxdeployment.yaml
 2109  diff viakustomize.yaml viakustomizewithawxdeployment.yaml
 2110  ls -lrt
 2111  cat viakustomize.yaml
 2112  cat viakustomizewithawxdeployment.yaml
 2113  vi awxk8s.yml
 2114  kubectl apply -f awxk8s.yml
 2115  kubectl apply -f awxk8s.yml -n awxtesting
 2116  kubectl apply -f awxk8s.yml
 2117  kubectl get services -n awx-demo
 2118  kubectl get po -n awx-demo
 2119  kubectl get pods -n awxtesting
 2120  ls -lrt
 2121  kubectl apply -f viakustomizewithawxdeployment.yaml
 2122  kubectl get po -n awx-demo
 2123  kubectl logs -f deployments/awx-operator-controller-manager -c awx-manager -n awx-demo
 2124  kubectl logs -f deployments/awx-operator-controller-manager -c awx-manager -n awxtesting
 2125  ls
 2126  ls -lrt
 2127  vi viakustomizewithawxdeployment.yaml
 2128  kubectl get po -n awx
 2129  kubectl logs -f deployments/awx-operator-controller-manager -c awx-manager -n awxtesting
 2130  kubectl describe po awx-demo-844f8684c5-km8hw -n awx
 2131  kubectl get po -n awx
 2132  kubectl get services -n awx
 2133  vi ingress.yaml
 2134  kubectl apply -f ingress.yaml -n awx
 2135  vi ingress.yaml
 2136  k9s
 2137  history

