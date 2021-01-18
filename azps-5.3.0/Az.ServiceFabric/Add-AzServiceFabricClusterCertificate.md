---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525453"
---
# <span data-ttu-id="64b5b-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="64b5b-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="64b5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="64b5b-103">Lägg till ett sekundärt kluster certifikat i klustret.</span><span class="sxs-lookup"><span data-stu-id="64b5b-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="64b5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64b5b-104">SYNTAX</span></span>

### <span data-ttu-id="64b5b-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="64b5b-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b5b-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="64b5b-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b5b-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="64b5b-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64b5b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64b5b-108">DESCRIPTION</span></span>
<span data-ttu-id="64b5b-109">Använd **Add-AzServiceFabricClusterCertificate** för att lägga till ett sekundärt kluster certifikat, antingen från ett befintligt Azure Key-valv eller skapa ett nytt Azure-valv med ett befintligt certifikat som tillhandahålls eller från ett nytt självsignerat certifikat som har skapats.</span><span class="sxs-lookup"><span data-stu-id="64b5b-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="64b5b-110">Det sekundära klustret åsidosätts om det finns något.</span><span class="sxs-lookup"><span data-stu-id="64b5b-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="64b5b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64b5b-111">EXAMPLES</span></span>

### <span data-ttu-id="64b5b-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="64b5b-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="64b5b-113">Det här kommandot lägger till ett certifikat i det befintliga Azure Key-valvet som ett sekundärt kluster certifikat.</span><span class="sxs-lookup"><span data-stu-id="64b5b-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="64b5b-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="64b5b-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="64b5b-115">Det här kommandot skapar ett självsignerat certifikat i Azure Key Vault och uppgraderar klustret så att det används som sekundärt kluster certifikat.</span><span class="sxs-lookup"><span data-stu-id="64b5b-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="64b5b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64b5b-116">PARAMETERS</span></span>

### <span data-ttu-id="64b5b-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="64b5b-117">-CertificateCommonName</span></span>
<span data-ttu-id="64b5b-118">Certifikatets nätverks namn</span><span class="sxs-lookup"><span data-stu-id="64b5b-118">Certificate common name</span></span>

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

### <span data-ttu-id="64b5b-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="64b5b-119">-CertificateFile</span></span>
<span data-ttu-id="64b5b-120">Sökvägen till det befintliga certifikatet</span><span class="sxs-lookup"><span data-stu-id="64b5b-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="64b5b-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="64b5b-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="64b5b-122">Certifikat utfärdarens tumavtryck, avgränsade med kommatecken om fler än en</span><span class="sxs-lookup"><span data-stu-id="64b5b-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="64b5b-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="64b5b-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="64b5b-124">Den mapp där det nya certifikatet behöver hämtas.</span><span class="sxs-lookup"><span data-stu-id="64b5b-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="64b5b-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="64b5b-125">-CertificatePassword</span></span>
<span data-ttu-id="64b5b-126">Lösen ordet för certifikatet</span><span class="sxs-lookup"><span data-stu-id="64b5b-126">The password of the certificate</span></span>

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

### <span data-ttu-id="64b5b-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="64b5b-127">-CertificateSubjectName</span></span>
<span data-ttu-id="64b5b-128">Certifikatets ämnes namn</span><span class="sxs-lookup"><span data-stu-id="64b5b-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="64b5b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b5b-129">-DefaultProfile</span></span>
<span data-ttu-id="64b5b-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64b5b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b5b-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="64b5b-131">-KeyVaultName</span></span>
<span data-ttu-id="64b5b-132">Namn på Azure-valv om det inte anges blir det standard namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="64b5b-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="64b5b-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b5b-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="64b5b-134">Resurs grupp namn för Azure-valv om det inte anges blir det standard för resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="64b5b-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="64b5b-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="64b5b-135">-Name</span></span>
<span data-ttu-id="64b5b-136">Ange namnet på klustret</span><span class="sxs-lookup"><span data-stu-id="64b5b-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="64b5b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b5b-137">-ResourceGroupName</span></span>
<span data-ttu-id="64b5b-138">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="64b5b-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="64b5b-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="64b5b-139">-SecretIdentifier</span></span>
<span data-ttu-id="64b5b-140">Den befintliga hemliga URL-adressen för Azure Key Vault, till exempel " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="64b5b-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="64b5b-141">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="64b5b-141">-Thumbprint</span></span>
<span data-ttu-id="64b5b-142">Tumavtrycket för certifikatet correspoinding till SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="64b5b-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="64b5b-143">Använd det här alternativet om certifikatet inte är hanterat eftersom nyckel valvet bara har certifikatet lagrat som hemligt och cmdleten inte kan hämta tumavtrycket.</span><span class="sxs-lookup"><span data-stu-id="64b5b-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64b5b-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="64b5b-144">-Confirm</span></span>
<span data-ttu-id="64b5b-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64b5b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64b5b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b5b-146">-WhatIf</span></span>
<span data-ttu-id="64b5b-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64b5b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b5b-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="64b5b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64b5b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b5b-149">CommonParameters</span></span>
<span data-ttu-id="64b5b-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64b5b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b5b-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64b5b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b5b-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64b5b-152">INPUTS</span></span>

### <span data-ttu-id="64b5b-153">System. String</span><span class="sxs-lookup"><span data-stu-id="64b5b-153">System.String</span></span>

### <span data-ttu-id="64b5b-154">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="64b5b-154">System.Security.SecureString</span></span>

## <span data-ttu-id="64b5b-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64b5b-155">OUTPUTS</span></span>

### <span data-ttu-id="64b5b-156">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="64b5b-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="64b5b-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64b5b-157">NOTES</span></span>

## <span data-ttu-id="64b5b-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64b5b-158">RELATED LINKS</span></span>

[<span data-ttu-id="64b5b-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="64b5b-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="64b5b-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="64b5b-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
