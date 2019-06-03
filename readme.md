Your Kubernetes master has initialized successfully!

To start using your cluster, you need to run the following as a regular user:

  mkdir -p $HOME/.kube
  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
  sudo chown $(id -u):$(id -g) $HOME/.kube/config

You should now deploy a pod network to the cluster.
Run "kubectl apply -f [podnetwork].yaml" with one of the options listed at:
  https://kubernetes.io/docs/concepts/cluster-administration/addons/

You can now join any number of machines by running the following on each node
as root:

  kubeadm join 172.28.128.4:6443 --token kdoap5.fduaxaqukbpsm7xs --discovery-token-ca-cert-hash sha256:46214dd65f3964d4b0541cf6280fde21bf056eb4d8e1d49a7df2daf787466d23

  
  apiVersion: v1
clusters:
- cluster:
    certificate-authority-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUN5RENDQWJDZ0F3SUJBZ0lCQURBTkJna3Foa2lHOXcwQkFRc0ZBREFWTVJNd0VRWURWUVFERXdwcmRXSmwKY201bGRHVnpNQjRYRFRFNE1UQXlNekl3TkRrd01sb1hEVEk0TVRBeU1ESXdORGt3TWxvd0ZURVRNQkVHQTFVRQpBeE1LYTNWaVpYSnVaWFJsY3pDQ0FTSXdEUVlKS29aSWh2Y05BUUVCQlFBRGdnRVBBRENDQVFvQ2dnRUJBTW5HCkd0Qm9QR2tqL0xyN3FkaHJCYitTb1h0UkdIR091TjlhUFZEQ2tHZ2MvaTAxZHpDM0pmbzM0dlNHOWNySTRWbVIKVzlDSWhMU1N6OTg2ODZOVWZzaU5qMzJBaTYvdGNTM0ZnamxzaTlDU01BcnJrSUdLaFJ1b2ppcFBFZWE2R0oxTgpRR09USWg2bGZkUFpFSzBvQy9uV0E2WTFDU0JVZm9aeWZKaTVsRzhDakRaOTlCN2pvM2FmdmgyNjJub2RJV0w5CjBWNHo2Si9yNzhqUng5Ui9kTEJNakZ1MEtweCtzK2xlYWcrdDVSckx6cHZzM2xTVm5OTGtoMGljcGRlY1QzMHcKUU9oQkovWTRtcHRsaGpSaktNaDlzQWFoQzRzNHV4UElqTHVrSDVNY3dmMDQ0NjFNRW90U1dsY1Q3Z2xENWJLWQpyRmJSSmZGWVhiODJ3Z09qUnJzQ0F3RUFBYU1qTUNFd0RnWURWUjBQQVFIL0JBUURBZ0trTUE4R0ExVWRFd0VCCi93UUZNQU1CQWY4d0RRWUpLb1pJaHZjTkFRRUxCUUFEZ2dFQkFMK1VQUGV2RWtXbGFJTVFTMlVHb3BudU5oOHAKeXZyZTZESGZGRjE2Z0dlNmZsc0dlOFgwMjUwRzhMSzgvOUpiZXJOKzNWMmozeXlaZ1pJUHRKSXZtaVduU1JTMgpqaUc1bGt0SlpDTTlyWEprSFRrdUMrQzRPRzRrYlFoQ0xETnh0SGNDanpuRjQyV0VUQ0FiQ0ZEUGdnU2xJZjRBCnRuck1TWGhicW1IbDk3WWNmak9UejI1b21ZN3B5SGIwa1h4bHkybWQxeDc2NUhxRkZLazBYQWpVU0ZFMDdaSW8KQnhqdjNVR0RYMjJZay9NSVdDSzR1SU9BbUZlS3BGczJQZnFQd0tGQWZkWmNTMkM4Q2JpaHV0T0QyNzV5WkZSdQpKTHdmZ0x1clNHZXUzUlEwbFRoZWw1U01SNjJxcGpJZWlWUVZaS1ZiNTZINDI5YytpcDltVTVvRHVZTT0KLS0tLS1FTkQgQ0VSVElGSUNBVEUtLS0tLQo=
    server: https://172.28.128.4:6443
  name: kubernetes
contexts:
- context:
    cluster: kubernetes
    user: kubernetes-admin
  name: kubernetes-admin@kubernetes
current-context: kubernetes-admin@kubernetes
kind: Config
preferences: {}
users:
- name: kubernetes-admin
  user:
    client-certificate-data: LS0tLS1CRUdJTiBDRVJUSUZJQ0FURS0tLS0tCk1JSUM4akNDQWRxZ0F3SUJBZ0lJYS9SeFgreU5IdG93RFFZSktvWklodmNOQVFFTEJRQXdGVEVUTUJFR0ExVUUKQXhNS2EzVmlaWEp1WlhSbGN6QWVGdzB4T0RFd01qTXlNRFE1TURKYUZ3MHhPVEV3TWpNeU1EUTVNRE5hTURReApGekFWQmdOVkJBb1REbk41YzNSbGJUcHRZWE4wWlhKek1Sa3dGd1lEVlFRREV4QnJkV0psY201bGRHVnpMV0ZrCmJXbHVNSUlCSWpBTkJna3Foa2lHOXcwQkFRRUZBQU9DQVE4QU1JSUJDZ0tDQVFFQXBsVGttMVJRbHNQaVcxeUoKZlc1TllFT3pmSmhxU05lUE0vOUZVVTB2TXJKUlZtQXE3emRxbFl5SGZHM1dmMG54MkwxRTc4MmI2M01sakp5YwpKZCtIVTY3alFqUGhSak9DYnRaWFhnc2dPcVFiMjJUdmtKQ0t5dFdTd3BXWEl4K2hvQ2RDTEpod0R4ZitTMHZYCmRKMUdrKzJoejZTbEZXWHI5SUoveC8wM3MrUUpEL09iaDRmaUx6UFFmdEdsQktjTTZRQkhCTHV5aitiNVpPN1YKVjNmdVUwOEVvWnUzbE1jcEhQdGtaZVJGMUFsTE9pUCtpd0tSbDdtZHhVUFZFU0dzN1RxRndKTHBkNlBVQXBoRApXNlROZmJiLzM2OG1MTHNsd3JWdTJEK2dKdUY0Y0F2VjBBQWZRQzFSU1VHZnlLaWszNmFUSFYzNVhUY2Myb2h2CmZBcVhod0lEQVFBQm95Y3dKVEFPQmdOVkhROEJBZjhFQkFNQ0JhQXdFd1lEVlIwbEJBd3dDZ1lJS3dZQkJRVUgKQXdJd0RRWUpLb1pJaHZjTkFRRUxCUUFEZ2dFQkFIeG4zQ0gwcmVEVXlMQnFYZkJka1U3WHhtem5SZVY0bENFcQptMUFLTHJFbUtIdFJFK2FCdWxwdjFQTVFBc3BheGFKREd6ZXk2Q0VIQTlkM2hDeVRBTHZEZGRaaHdRMXZVR2JRCkMrcVZIL01GcFNKMjhoMk96VkcyVWFYalZTT25hWk9UMkR3bUk0MXNmNURocVJZYi9zSUIxNXdHZWFRbEZ3b1kKWGFITFFmTWdNVC9VRWxqcG9MYTdHMDNGQjJEeGw2VkZzYVE1SDg2T3ZOMXRLNy9zdWM4MEFwSWhpNEl0ckJoQgpySWdyYXB0QlJOcGZtUUxsc3VsMUZVUklEektSYStPbmxuN0JTWDVVczlRUHNaS1Naa0ZKUDFNYUJzVW9IWC8rCkpVWW51dFYrSG9LM1R6c1FPSko4cWhjOGY5VS9tdEU4REZpdWRTSzBWV2FGbmdJRG1OZz0KLS0tLS1FTkQgQ0VSVElGSUNBVEUtLS0tLQo=
    client-key-data: LS0tLS1CRUdJTiBSU0EgUFJJVkFURSBLRVktLS0tLQpNSUlFcFFJQkFBS0NBUUVBcGxUa20xUlFsc1BpVzF5SmZXNU5ZRU96ZkpocVNOZVBNLzlGVVUwdk1ySlJWbUFxCjd6ZHFsWXlIZkczV2YwbngyTDFFNzgyYjYzTWxqSnljSmQrSFU2N2pRalBoUmpPQ2J0WlhYZ3NnT3FRYjIyVHYKa0pDS3l0V1N3cFdYSXgraG9DZENMSmh3RHhmK1MwdlhkSjFHaysyaHo2U2xGV1hyOUlKL3gvMDNzK1FKRC9PYgpoNGZpTHpQUWZ0R2xCS2NNNlFCSEJMdXlqK2I1Wk83VlYzZnVVMDhFb1p1M2xNY3BIUHRrWmVSRjFBbExPaVArCml3S1JsN21keFVQVkVTR3M3VHFGd0pMcGQ2UFVBcGhEVzZUTmZiYi8zNjhtTExzbHdyVnUyRCtnSnVGNGNBdlYKMEFBZlFDMVJTVUdmeUtpazM2YVRIVjM1WFRjYzJvaHZmQXFYaHdJREFRQUJBb0lCQUFELy9hZlpaK3FnSHRwQgp3aW5ZNGVvMFBmMy94SlBQaC9MZUZBS2JIaStGMXV0WUJLb1BnVHFJNzcrVndYWmVjVy9HSTRYMWpIeHI0c3ZuCm5TQzFLVkVkZWd4SjE0N2VmR2hDTGFCSkhOWjlhaFYxaytNZ20xVUExN01IeHpMVTI5bmtvb2MyRzJaYjFKR0wKVVM1SVM4WlQ1V2NrTEVIbXJQWjVXbDlQYkdoT2Npck1TSlN2N2NkeXR2d2dWaUoyZ0NqZm03d1JkdHFMR05KdQpTNVBHeTZ6RFM5WkdTRXQ2c3lDNHh3bHB3MCsyOW0yZnA2WjlHdTZGSU5lR24yUWFLcnpqandMdzRmcCsraHJuCkN0WTIxYXVzRjlYU1BqMVpkNnlGQ0JUTUozaHp5cWdnQnBodGpOWUpoODcxaXczQUpERWdQVGNaUGpnSlZnbTkKMWNFVGtnRUNnWUVBM1N1aU1BV0E2YkJUUVpVczdwdG5TR1pmQzFnSUt0aEw1K3kxV2ZlN0NpYUo5WEE1MUpCagphNCs1OW96TytwNVcza3pvK2xLc2hmZzk4SEpQdklDd240L2NuQTNWNkYweE9pQ1lTQUJrUG1Eb1M5QzZMVmNYCnN1VTdsMCs5Z1EyQXlaazJySEZoNlNQSENIbCtCMkMvOERwUmthS2xNRVRjSXFVRWhENDFNNEVDZ1lFQXdJWjIKTlprV1F2aTFaTWhNTFhIdXkyb1hGMys5VTd1SlNhZVVjTzV3aytTcXJnS0Y1eElKcmxWd1hpRlZ6RExyZ3FNYgpBRHB4dGhtWXJqTFFhZllXMTJaRlNZazVLSDNqUkRIU3EwVmYwbHRXSzZyWVYvWlE2bTFDMzNEMjV0T3ZPejBNCmtsVnRUeEhEOHJvWURkR3czV2Y1MGRRV3l0emVMWDBSNUNiaHJ3Y0NnWUVBbS9odWF5RW1kU2FVd0JZOFZwU2YKTkk2RkRsSHBpSlY2aWpjQytVeGJ5ZCs5d0ttQkR1YzRSWjFaRG9ia1hCY1h1Yk5SUlY3U0xiUVBzaVpiRnR0RwpNM0JYcW5HVFhVZUROTFBSMEV6K1pJTWdybjZuSE54amFSU0Jmc2FNSkp0cUxFRnhMaERUZEg5M21BRmRvRVJaCmQwY1pTUFFEUEZRRFRpZERWU010ajRFQ2dZRUFsWFRNdDNjTUxSbGQxOHNXT0FGR1cyc1VXZzIwTUJoWnoyL2sKY0hicHRpWEJ5aXZ6UHhwbG9ZeDZHdGpOL2lOWmFLU3VCVk5aaXYvNzR0OVhvNnFDdU55UDFUSk55UDFSUEZOaApNOHc3UXRYYzR6RlJtWmVCNFRySXV5UzZ4eDUxM2dyYWc0OEZ1R2dXTVl2OXVGeWNiSVNYRHlrU09KR1ZlTUtxCjdPNnlMR2tDZ1lFQXMxTHBrRDkzUkJKTzBoa1ZyOGVEMldJNUNjSnBQcWk5Z3pGUjZITWZDdTZPRjR6ZFI1aG8KK2xpV1JPdE5iU1J1MGhVRkdmcUZJTXFtVG9IMHoxZEhpR1BlNUw2RVBNci9ibkc3dUtBVUlkamV4TFFJUG1oMAplR3gxVEQ5R1VIZys3bGZkeTdKMHU2OTRpWTRYZzlESW1vYzVjUUVqQzd4d29KTEFWbTBMMGhVPQotLS0tLUVORCBSU0EgUFJJVkFURSBLRVktLS0tLQo=
# k8s-vagrant-ansible-centos
