---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 58547205bc0edae3ea1ab9ff56d3df1ef71214f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746852"
---
# <span data-ttu-id="3581a-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="3581a-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="3581a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3581a-102">SYNOPSIS</span></span>
<span data-ttu-id="3581a-103">Lägg till ett nytt certifikat till den virtuella datorns skal uppsättning (er) som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="3581a-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="3581a-104">Certifikatet är avsett att användas som ett program certifikat.</span><span class="sxs-lookup"><span data-stu-id="3581a-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="3581a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3581a-105">SYNTAX</span></span>

### <span data-ttu-id="3581a-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="3581a-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3581a-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="3581a-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3581a-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="3581a-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3581a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3581a-109">DESCRIPTION</span></span>
<span data-ttu-id="3581a-110">Använd **Add-AzServiceFabricApplicationCertificate** för att installera ett certifikat för alla noder i klustret.</span><span class="sxs-lookup"><span data-stu-id="3581a-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="3581a-111">Du kan ange ett certifikat som du redan har eller låta systemet skapa ett nytt för dig och överföra det till ett nytt eller befintligt Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="3581a-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="3581a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3581a-112">EXAMPLES</span></span>

### <span data-ttu-id="3581a-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3581a-113">Example 1</span></span>
```
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="3581a-114">Det här kommandot lägger till ett certifikat från ett befintligt Azure Key-valv till alla nodtyper i klustret.</span><span class="sxs-lookup"><span data-stu-id="3581a-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="3581a-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3581a-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="3581a-116">Det här kommandot skapar ett självsignerat certifikat i Azure-valvet med nyckelordet Key valv resurs grupp namn och valv namn, installerar till alla nodtyper för klustret och hämtar certifikatet under mappen "c:\test".</span><span class="sxs-lookup"><span data-stu-id="3581a-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="3581a-117">Namnet på det hämtade certifikatet är samma som namnet på Key valv-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3581a-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="3581a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3581a-118">PARAMETERS</span></span>

### <span data-ttu-id="3581a-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="3581a-119">-CertificateCommonName</span></span>
<span data-ttu-id="3581a-120">Certifikatets nätverks namn</span><span class="sxs-lookup"><span data-stu-id="3581a-120">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3581a-121">-CertificateFile</span></span>
<span data-ttu-id="3581a-122">Befintlig sökväg till certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="3581a-122">The existing certificate file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="3581a-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="3581a-124">Certifikat utfärdarens tumavtryck, avgränsade med kommatecken om fler än en</span><span class="sxs-lookup"><span data-stu-id="3581a-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="3581a-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="3581a-126">Sökvägen till det nya certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3581a-126">The folder path of the new certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3581a-127">-CertificatePassword</span></span>
<span data-ttu-id="3581a-128">Lösen ordet för PFX-filen.</span><span class="sxs-lookup"><span data-stu-id="3581a-128">The password of the pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="3581a-129">-CertificateSubjectName</span></span>
<span data-ttu-id="3581a-130">DNS-namnet på certifikatet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3581a-130">The Dns name of the certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3581a-131">-DefaultProfile</span></span>
<span data-ttu-id="3581a-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3581a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3581a-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="3581a-133">-KeyVaultName</span></span>
<span data-ttu-id="3581a-134">Namn på Azure Key valv.</span><span class="sxs-lookup"><span data-stu-id="3581a-134">Azure key vault name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-135">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="3581a-135">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="3581a-136">Namnet på Azure Key valv-resursen.</span><span class="sxs-lookup"><span data-stu-id="3581a-136">Azure key vault resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="3581a-137">-Name</span></span>
<span data-ttu-id="3581a-138">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="3581a-138">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3581a-139">-ResourceGroupName</span></span>
<span data-ttu-id="3581a-140">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3581a-140">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="3581a-141">-SecretIdentifier</span></span>
<span data-ttu-id="3581a-142">Den befintliga Azure Key Vault Secret URI.</span><span class="sxs-lookup"><span data-stu-id="3581a-142">The existing Azure key vault secret uri.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3581a-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3581a-143">-Confirm</span></span>
<span data-ttu-id="3581a-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3581a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3581a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3581a-145">-WhatIf</span></span>
<span data-ttu-id="3581a-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3581a-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3581a-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3581a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3581a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3581a-148">CommonParameters</span></span>
<span data-ttu-id="3581a-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3581a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3581a-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3581a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3581a-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3581a-151">INPUTS</span></span>

### <span data-ttu-id="3581a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3581a-152">System.String</span></span>

### <span data-ttu-id="3581a-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="3581a-153">System.Security.SecureString</span></span>

## <span data-ttu-id="3581a-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3581a-154">OUTPUTS</span></span>

### <span data-ttu-id="3581a-155">Microsoft. Azure. commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3581a-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="3581a-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3581a-156">NOTES</span></span>

## <span data-ttu-id="3581a-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3581a-157">RELATED LINKS</span></span>

[<span data-ttu-id="3581a-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3581a-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="3581a-159">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3581a-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
