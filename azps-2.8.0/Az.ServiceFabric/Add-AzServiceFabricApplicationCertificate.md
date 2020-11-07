---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 62298a5747a8bb5b4f01458cac611f5e86869ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919942"
---
# <span data-ttu-id="43826-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="43826-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="43826-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43826-102">SYNOPSIS</span></span>
<span data-ttu-id="43826-103">Lägg till ett nytt certifikat till den virtuella datorns skal uppsättning (er) som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="43826-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="43826-104">Certifikatet är avsett att användas som ett program certifikat.</span><span class="sxs-lookup"><span data-stu-id="43826-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="43826-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43826-105">SYNTAX</span></span>

### <span data-ttu-id="43826-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="43826-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43826-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="43826-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43826-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="43826-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43826-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43826-109">DESCRIPTION</span></span>
<span data-ttu-id="43826-110">Använd **Add-AzServiceFabricApplicationCertificate** för att installera ett certifikat för alla noder i klustret.</span><span class="sxs-lookup"><span data-stu-id="43826-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="43826-111">Du kan ange ett certifikat som du redan har eller låta systemet skapa ett nytt för dig och överföra det till ett nytt eller befintligt Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="43826-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="43826-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43826-112">EXAMPLES</span></span>

### <span data-ttu-id="43826-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="43826-113">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="43826-114">Det här kommandot lägger till ett certifikat från ett befintligt Azure Key-valv till alla nodtyper i klustret.</span><span class="sxs-lookup"><span data-stu-id="43826-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="43826-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="43826-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="43826-116">Det här kommandot skapar ett självsignerat certifikat i Azure-valvet med nyckelordet Key valv resurs grupp namn och valv namn, installerar till alla nodtyper för klustret och hämtar certifikatet under mappen "c:\test".</span><span class="sxs-lookup"><span data-stu-id="43826-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="43826-117">Namnet på det hämtade certifikatet är samma som namnet på Key valv-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="43826-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="43826-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43826-118">PARAMETERS</span></span>

### <span data-ttu-id="43826-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="43826-119">-CertificateCommonName</span></span>
<span data-ttu-id="43826-120">Certifikatets nätverks namn</span><span class="sxs-lookup"><span data-stu-id="43826-120">Certificate common name</span></span>

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

### <span data-ttu-id="43826-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="43826-121">-CertificateFile</span></span>
<span data-ttu-id="43826-122">Sökvägen till det befintliga certifikatet</span><span class="sxs-lookup"><span data-stu-id="43826-122">The path to the existing certificate</span></span>

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

### <span data-ttu-id="43826-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="43826-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="43826-124">Certifikat utfärdarens tumavtryck, avgränsade med kommatecken om fler än en</span><span class="sxs-lookup"><span data-stu-id="43826-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="43826-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="43826-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="43826-126">Den mapp där det nya certifikatet behöver hämtas.</span><span class="sxs-lookup"><span data-stu-id="43826-126">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="43826-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="43826-127">-CertificatePassword</span></span>
<span data-ttu-id="43826-128">Lösen ordet för certifikatet</span><span class="sxs-lookup"><span data-stu-id="43826-128">The password of the certificate</span></span>

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

### <span data-ttu-id="43826-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="43826-129">-CertificateSubjectName</span></span>
<span data-ttu-id="43826-130">Certifikatets ämnes namn</span><span class="sxs-lookup"><span data-stu-id="43826-130">The subject name of the certificate</span></span>

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

### <span data-ttu-id="43826-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43826-131">-DefaultProfile</span></span>
<span data-ttu-id="43826-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43826-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43826-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="43826-133">-KeyVaultName</span></span>
<span data-ttu-id="43826-134">Namn på Azure-valv om det inte anges blir det standard namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="43826-134">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="43826-135">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43826-135">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="43826-136">Resurs grupp namn för Azure-valv om det inte anges blir det standard för resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="43826-136">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43826-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="43826-137">-Name</span></span>
<span data-ttu-id="43826-138">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="43826-138">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="43826-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43826-139">-ResourceGroupName</span></span>
<span data-ttu-id="43826-140">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="43826-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="43826-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="43826-141">-SecretIdentifier</span></span>
<span data-ttu-id="43826-142">Den befintliga hemliga URL-adressen för Azure Key Vault, till exempel " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="43826-142">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="43826-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43826-143">-Confirm</span></span>
<span data-ttu-id="43826-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43826-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43826-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43826-145">-WhatIf</span></span>
<span data-ttu-id="43826-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43826-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43826-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43826-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43826-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43826-148">CommonParameters</span></span>
<span data-ttu-id="43826-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43826-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43826-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43826-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43826-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43826-151">INPUTS</span></span>

### <span data-ttu-id="43826-152">System. String</span><span class="sxs-lookup"><span data-stu-id="43826-152">System.String</span></span>

### <span data-ttu-id="43826-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="43826-153">System.Security.SecureString</span></span>

## <span data-ttu-id="43826-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43826-154">OUTPUTS</span></span>

### <span data-ttu-id="43826-155">Microsoft. Azure. commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="43826-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="43826-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43826-156">NOTES</span></span>

## <span data-ttu-id="43826-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43826-157">RELATED LINKS</span></span>

[<span data-ttu-id="43826-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="43826-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="43826-159">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="43826-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
