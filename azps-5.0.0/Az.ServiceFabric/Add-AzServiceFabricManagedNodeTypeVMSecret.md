---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263408"
---
# <span data-ttu-id="b1012-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="b1012-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="b1012-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1012-102">SYNOPSIS</span></span>
<span data-ttu-id="b1012-103">Lägg till certifikat hemlighet till nodtyp.</span><span class="sxs-lookup"><span data-stu-id="b1012-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="b1012-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1012-104">SYNTAX</span></span>

### <span data-ttu-id="b1012-105">ByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="b1012-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1012-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b1012-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1012-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1012-107">DESCRIPTION</span></span>
<span data-ttu-id="b1012-108">Lägg till certifikat hemlighet till nodtyp.</span><span class="sxs-lookup"><span data-stu-id="b1012-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="b1012-109">Hemligheten måste lagras i ett Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="b1012-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="b1012-110">Mer information om viktiga valv finns i vad är Azure Key Vault?</span><span class="sxs-lookup"><span data-stu-id="b1012-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="b1012-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="b1012-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="b1012-112">Mer information om cmdletar finns i cmdlets för Azure Key Vault ( https://msdn.microsoft.com/library/azure/dn868052.aspx) i Microsoft Developer Network Library eller Set-AzKeyVaultSecret cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1012-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="b1012-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1012-113">EXAMPLES</span></span>

### <span data-ttu-id="b1012-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b1012-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="b1012-115">Den här kommatecknet lägger till en certifikat hemlighet från det angivna nyckel valvet och den hemliga identifieraren.</span><span class="sxs-lookup"><span data-stu-id="b1012-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="b1012-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b1012-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="b1012-117">Den här kommatecknet lägger till en certifikat hemlighet från nyckel valvet och den hemliga identifieraren, med rör.</span><span class="sxs-lookup"><span data-stu-id="b1012-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="b1012-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1012-118">PARAMETERS</span></span>

### <span data-ttu-id="b1012-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1012-119">-AsJob</span></span>
<span data-ttu-id="b1012-120">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="b1012-120">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="b1012-121">-CertificateStore</span></span>
<span data-ttu-id="b1012-122">Anger certifikat arkivet på den virtuella dator där certifikatet ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="b1012-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="b1012-123">Det angivna certifikat arkivet är implicit i LocalMachine-kontot.</span><span class="sxs-lookup"><span data-stu-id="b1012-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="b1012-124">-CertificateUrl</span></span>
<span data-ttu-id="b1012-125">Det här är URL-adressen till ett certifikat som har laddats upp till nyckel Valve som en hemlighet.</span><span class="sxs-lookup"><span data-stu-id="b1012-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="b1012-126">Information om hur du lägger till en hemlighet till nyckel valvet finns i \[ lägga till en nyckel eller en hemlighet i nyckel valvet \] ( https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="b1012-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="b1012-127">I det här fallet måste ditt certifikat vara det är base64-kodningen för följande JSON-objekt som är kodad i UTF-8: \<br\> \<br\> { \<br\> "data": " \<Base64-encoded-certificate\> ", \<br\> "datatyp": "PFX", \<br\> "lösen ord": " \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="b1012-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-128">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="b1012-128">-ClusterName</span></span>
<span data-ttu-id="b1012-129">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="b1012-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1012-130">-DefaultProfile</span></span>
<span data-ttu-id="b1012-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1012-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1012-132">-InputObject</span></span>
<span data-ttu-id="b1012-133">Resurs för nodtyp</span><span class="sxs-lookup"><span data-stu-id="b1012-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="b1012-134">-Name</span></span>
<span data-ttu-id="b1012-135">Ange namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="b1012-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1012-136">-ResourceGroupName</span></span>
<span data-ttu-id="b1012-137">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b1012-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b1012-138">-SourceVaultId</span></span>
<span data-ttu-id="b1012-139">ID för Key valv-resurs som innehåller certifikaten.</span><span class="sxs-lookup"><span data-stu-id="b1012-139">Key Vault resource id containing the certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b1012-140">-Confirm</span></span>
<span data-ttu-id="b1012-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1012-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1012-142">-WhatIf</span></span>
<span data-ttu-id="b1012-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b1012-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1012-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b1012-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1012-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1012-145">CommonParameters</span></span>
<span data-ttu-id="b1012-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1012-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1012-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1012-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1012-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1012-148">INPUTS</span></span>

### <span data-ttu-id="b1012-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b1012-149">System.String</span></span>

## <span data-ttu-id="b1012-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1012-150">OUTPUTS</span></span>

### <span data-ttu-id="b1012-151">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="b1012-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="b1012-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1012-152">NOTES</span></span>

## <span data-ttu-id="b1012-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1012-153">RELATED LINKS</span></span>
