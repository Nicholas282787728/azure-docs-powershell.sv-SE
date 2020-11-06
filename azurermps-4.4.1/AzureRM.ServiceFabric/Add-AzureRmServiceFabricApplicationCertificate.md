---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 6d77c795415bca1a8bffbed6d09062f394782e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583768"
---
# <span data-ttu-id="d7c63-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="d7c63-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="d7c63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7c63-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c63-103">Lägg till ett nytt certifikat till den virtuella datorns skal uppsättning (er) som utgör klustret.</span><span class="sxs-lookup"><span data-stu-id="d7c63-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="d7c63-104">Certifikatet är avsett att användas som ett program certifikat.</span><span class="sxs-lookup"><span data-stu-id="d7c63-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7c63-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7c63-105">SYNTAX</span></span>

### <span data-ttu-id="d7c63-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7c63-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7c63-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="d7c63-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7c63-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="d7c63-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7c63-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7c63-109">DESCRIPTION</span></span>
<span data-ttu-id="d7c63-110">Använd **Add-AzureRmServiceFabricApplicationCertificate** för att installera ett certifikat för alla noder i klustret.</span><span class="sxs-lookup"><span data-stu-id="d7c63-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="d7c63-111">Du kan ange ett certifikat som du redan har eller låta systemet skapa ett nytt för dig och överföra det till ett nytt eller befintligt Azure Key-valv.</span><span class="sxs-lookup"><span data-stu-id="d7c63-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="d7c63-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7c63-112">EXAMPLES</span></span>

### <span data-ttu-id="d7c63-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d7c63-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="d7c63-114">Det här kommandot lägger till ett certifikat från ett befintligt Azure Key-valv till alla nodtyper i klustret.</span><span class="sxs-lookup"><span data-stu-id="d7c63-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="d7c63-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d7c63-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="d7c63-116">Det här kommandot skapar ett självsignerat certifikat i Azure-valvet med nyckelordet Key valv resurs grupp namn och valv namn, installerar till alla nodtyper för klustret och hämtar certifikatet under mappen "c:\test".</span><span class="sxs-lookup"><span data-stu-id="d7c63-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="d7c63-117">Namnet på det hämtade certifikatet är samma som namnet på Key valv-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="d7c63-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="d7c63-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7c63-118">PARAMETERS</span></span>

### <span data-ttu-id="d7c63-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d7c63-119">-CertificateFile</span></span>
<span data-ttu-id="d7c63-120">Befintlig sökväg till certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="d7c63-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="d7c63-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="d7c63-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="d7c63-122">Sökvägen till det nya certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d7c63-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="d7c63-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d7c63-123">-CertificatePassword</span></span>
<span data-ttu-id="d7c63-124">Lösen ordet för PFX-filen.</span><span class="sxs-lookup"><span data-stu-id="d7c63-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="d7c63-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="d7c63-125">-CertificateSubjectName</span></span>
<span data-ttu-id="d7c63-126">DNS-namnet på certifikatet som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d7c63-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="d7c63-127">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="d7c63-127">-KeyVaultName</span></span>
<span data-ttu-id="d7c63-128">Namn på Azure Key valv.</span><span class="sxs-lookup"><span data-stu-id="d7c63-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="d7c63-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c63-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="d7c63-130">Namnet på Azure Key valv-resursen.</span><span class="sxs-lookup"><span data-stu-id="d7c63-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="d7c63-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7c63-131">-Name</span></span>
<span data-ttu-id="d7c63-132">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="d7c63-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d7c63-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c63-133">-ResourceGroupName</span></span>
<span data-ttu-id="d7c63-134">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d7c63-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d7c63-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="d7c63-135">-SecretIdentifier</span></span>
<span data-ttu-id="d7c63-136">Den befintliga Azure Key Vault Secret URI.</span><span class="sxs-lookup"><span data-stu-id="d7c63-136">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="d7c63-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d7c63-137">-Confirm</span></span>
<span data-ttu-id="d7c63-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d7c63-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7c63-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7c63-139">-WhatIf</span></span>
<span data-ttu-id="d7c63-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d7c63-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7c63-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d7c63-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7c63-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c63-142">-DefaultProfile</span></span>
<span data-ttu-id="d7c63-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7c63-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7c63-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c63-144">CommonParameters</span></span>
<span data-ttu-id="d7c63-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7c63-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c63-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7c63-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c63-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7c63-147">INPUTS</span></span>

### <span data-ttu-id="d7c63-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d7c63-148">System.String</span></span>

## <span data-ttu-id="d7c63-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7c63-149">OUTPUTS</span></span>

### <span data-ttu-id="d7c63-150">Microsoft. Azure. commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7c63-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="d7c63-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7c63-151">NOTES</span></span>

## <span data-ttu-id="d7c63-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7c63-152">RELATED LINKS</span></span>

[<span data-ttu-id="d7c63-153">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="d7c63-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="d7c63-154">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d7c63-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
