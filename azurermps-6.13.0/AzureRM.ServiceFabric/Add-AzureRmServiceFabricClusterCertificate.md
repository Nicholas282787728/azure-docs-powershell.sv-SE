---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: fa357a4f5b8e599858ce5aff3e0aa11121833ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577880"
---
# <span data-ttu-id="a9d37-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a9d37-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="a9d37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9d37-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d37-103">Lägg till ett sekundärt kluster certifikat i klustret.</span><span class="sxs-lookup"><span data-stu-id="a9d37-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9d37-104">SYNTAX</span></span>

### <span data-ttu-id="a9d37-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9d37-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9d37-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a9d37-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9d37-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a9d37-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9d37-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9d37-108">DESCRIPTION</span></span>
<span data-ttu-id="a9d37-109">Använd **Add-AzureRmServiceFabricClusterCertificate** för att lägga till ett sekundärt kluster certifikat, antingen från ett befintligt Azure Key-valv eller skapa ett nytt Azure-valv med ett befintligt certifikat som tillhandahålls eller från ett nytt självsignerat certifikat som har skapats.</span><span class="sxs-lookup"><span data-stu-id="a9d37-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="a9d37-110">Det sekundära klustret åsidosätts om det finns något.</span><span class="sxs-lookup"><span data-stu-id="a9d37-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="a9d37-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9d37-111">EXAMPLES</span></span>

### <span data-ttu-id="a9d37-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9d37-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="a9d37-113">Det här kommandot lägger till ett certifikat i det befintliga Azure Key-valvet som ett sekundärt kluster certifikat.</span><span class="sxs-lookup"><span data-stu-id="a9d37-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="a9d37-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a9d37-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="a9d37-115">Det här kommandot skapar ett självsignerat certifikat i Azure Key Vault och uppgraderar klustret så att det används som sekundärt kluster certifikat.</span><span class="sxs-lookup"><span data-stu-id="a9d37-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="a9d37-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9d37-116">PARAMETERS</span></span>

### <span data-ttu-id="a9d37-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a9d37-117">-CertificateFile</span></span>
<span data-ttu-id="a9d37-118">Befintlig sökväg till certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="a9d37-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="a9d37-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="a9d37-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="a9d37-120">Mappen för det nya certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a9d37-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="a9d37-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a9d37-121">-CertificatePassword</span></span>
<span data-ttu-id="a9d37-122">Lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="a9d37-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="a9d37-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="a9d37-123">-CertificateSubjectName</span></span>
<span data-ttu-id="a9d37-124">DNS-namnet på certifikatet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a9d37-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="a9d37-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d37-125">-DefaultProfile</span></span>
<span data-ttu-id="a9d37-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d37-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d37-127">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="a9d37-127">-KeyVaultName</span></span>
<span data-ttu-id="a9d37-128">Namn på Azure Key valv.</span><span class="sxs-lookup"><span data-stu-id="a9d37-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="a9d37-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d37-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="a9d37-130">Namnet på Azure Key valv-resursen.</span><span class="sxs-lookup"><span data-stu-id="a9d37-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="a9d37-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9d37-131">-Name</span></span>
<span data-ttu-id="a9d37-132">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="a9d37-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a9d37-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d37-133">-ResourceGroupName</span></span>
<span data-ttu-id="a9d37-134">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a9d37-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a9d37-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="a9d37-135">-SecretIdentifier</span></span>
<span data-ttu-id="a9d37-136">Den hemliga URL-adressen för Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a9d37-136">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="a9d37-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9d37-137">-Confirm</span></span>
<span data-ttu-id="a9d37-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9d37-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d37-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d37-139">-WhatIf</span></span>
<span data-ttu-id="a9d37-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9d37-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9d37-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9d37-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9d37-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d37-142">CommonParameters</span></span>
<span data-ttu-id="a9d37-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d37-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d37-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d37-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d37-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9d37-145">INPUTS</span></span>

### <span data-ttu-id="a9d37-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a9d37-146">System.String</span></span>
<span data-ttu-id="a9d37-147">Parametrar: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a9d37-147">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span></span>

### <span data-ttu-id="a9d37-148">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a9d37-148">System.Security.SecureString</span></span>
<span data-ttu-id="a9d37-149">Parametrar: CertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a9d37-149">Parameters: CertificatePassword (ByValue)</span></span>

## <span data-ttu-id="a9d37-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9d37-150">OUTPUTS</span></span>

### <span data-ttu-id="a9d37-151">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a9d37-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a9d37-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9d37-152">NOTES</span></span>

## <span data-ttu-id="a9d37-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9d37-153">RELATED LINKS</span></span>

[<span data-ttu-id="a9d37-154">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a9d37-154">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="a9d37-155">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a9d37-155">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="a9d37-156">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="a9d37-156">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
