---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746851"
---
# <span data-ttu-id="0ad2e-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0ad2e-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="0ad2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ad2e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad2e-103">Lägg till ett sekundärt kluster certifikat i klustret.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="0ad2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ad2e-104">SYNTAX</span></span>

### <span data-ttu-id="0ad2e-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="0ad2e-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad2e-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="0ad2e-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad2e-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="0ad2e-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ad2e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ad2e-108">DESCRIPTION</span></span>
<span data-ttu-id="0ad2e-109">Använd **Add-AzServiceFabricClusterCertificate** för att lägga till ett sekundärt kluster certifikat, antingen från ett befintligt Azure Key-valv eller skapa ett nytt Azure-valv med ett befintligt certifikat som tillhandahålls eller från ett nytt självsignerat certifikat som har skapats.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="0ad2e-110">Det sekundära klustret åsidosätts om det finns något.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="0ad2e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ad2e-111">EXAMPLES</span></span>

### <span data-ttu-id="0ad2e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0ad2e-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="0ad2e-113">Det här kommandot lägger till ett certifikat i det befintliga Azure Key-valvet som ett sekundärt kluster certifikat.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="0ad2e-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0ad2e-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="0ad2e-115">Det här kommandot skapar ett självsignerat certifikat i Azure Key Vault och uppgraderar klustret så att det används som sekundärt kluster certifikat.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="0ad2e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ad2e-116">PARAMETERS</span></span>

### <span data-ttu-id="0ad2e-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="0ad2e-117">-CertificateCommonName</span></span>
<span data-ttu-id="0ad2e-118">Certifikatets nätverks namn</span><span class="sxs-lookup"><span data-stu-id="0ad2e-118">Certificate common name</span></span>

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

### <span data-ttu-id="0ad2e-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0ad2e-119">-CertificateFile</span></span>
<span data-ttu-id="0ad2e-120">Befintlig sökväg till certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="0ad2e-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="0ad2e-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="0ad2e-122">Certifikat utfärdarens tumavtryck, avgränsade med kommatecken om fler än en</span><span class="sxs-lookup"><span data-stu-id="0ad2e-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="0ad2e-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="0ad2e-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="0ad2e-124">Mappen för det nya certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-124">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="0ad2e-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="0ad2e-125">-CertificatePassword</span></span>
<span data-ttu-id="0ad2e-126">Lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-126">The password of the certificate file.</span></span>

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

### <span data-ttu-id="0ad2e-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="0ad2e-127">-CertificateSubjectName</span></span>
<span data-ttu-id="0ad2e-128">DNS-namnet på certifikatet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-128">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="0ad2e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad2e-129">-DefaultProfile</span></span>
<span data-ttu-id="0ad2e-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ad2e-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="0ad2e-131">-KeyVaultName</span></span>
<span data-ttu-id="0ad2e-132">Namn på Azure Key valv.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-132">Azure key vault name.</span></span>

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

### <span data-ttu-id="0ad2e-133">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad2e-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="0ad2e-134">Namnet på Azure Key valv-resursen.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-134">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="0ad2e-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ad2e-135">-Name</span></span>
<span data-ttu-id="0ad2e-136">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-136">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0ad2e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad2e-137">-ResourceGroupName</span></span>
<span data-ttu-id="0ad2e-138">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0ad2e-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="0ad2e-139">-SecretIdentifier</span></span>
<span data-ttu-id="0ad2e-140">Den hemliga URL-adressen för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-140">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="0ad2e-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0ad2e-141">-Confirm</span></span>
<span data-ttu-id="0ad2e-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad2e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad2e-143">-WhatIf</span></span>
<span data-ttu-id="0ad2e-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ad2e-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad2e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad2e-146">CommonParameters</span></span>
<span data-ttu-id="0ad2e-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad2e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad2e-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad2e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad2e-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ad2e-149">INPUTS</span></span>

### <span data-ttu-id="0ad2e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad2e-150">System.String</span></span>

### <span data-ttu-id="0ad2e-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0ad2e-151">System.Security.SecureString</span></span>

## <span data-ttu-id="0ad2e-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ad2e-152">OUTPUTS</span></span>

### <span data-ttu-id="0ad2e-153">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0ad2e-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0ad2e-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ad2e-154">NOTES</span></span>

## <span data-ttu-id="0ad2e-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ad2e-155">RELATED LINKS</span></span>

[<span data-ttu-id="0ad2e-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0ad2e-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="0ad2e-157">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0ad2e-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="0ad2e-158">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="0ad2e-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
