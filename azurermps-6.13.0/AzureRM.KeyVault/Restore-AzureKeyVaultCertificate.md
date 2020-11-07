---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7955ecd02d40ac3dff891b8eb315a39ccf985ebb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757882"
---
# <span data-ttu-id="784cb-101">Restore-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="784cb-101">Restore-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="784cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="784cb-102">SYNOPSIS</span></span>
<span data-ttu-id="784cb-103">Återställer ett certifikat i ett nyckelord från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="784cb-103">Restores a certificate in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="784cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="784cb-104">SYNTAX</span></span>

### <span data-ttu-id="784cb-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="784cb-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="784cb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="784cb-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="784cb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="784cb-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="784cb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="784cb-108">DESCRIPTION</span></span>
<span data-ttu-id="784cb-109">Cmdleten **restore-AzureKeyVaultCertificate** skapar ett certifikat i det angivna nyckelvärdet från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="784cb-109">The **Restore-AzureKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="784cb-110">Det här certifikatet är en replik av säkerhetskopierat certifikat i indatafilen och har samma namn som det ursprungliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="784cb-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="784cb-111">Om det redan finns ett certifikat med samma namn i huvud valvet Miss lyckas denna cmdlet i stället för att skriva över det ursprungliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="784cb-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="784cb-112">Om säkerhets kopian innehåller flera versioner av ett certifikat återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="784cb-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="784cb-113">Det viktigaste valvet du återställer certifikatet till kan skilja sig från det huvud valv som du säkerhetskopierade certifikatet från.</span><span class="sxs-lookup"><span data-stu-id="784cb-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="784cb-114">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="784cb-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="784cb-115">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="784cb-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="784cb-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="784cb-116">EXAMPLES</span></span>

### <span data-ttu-id="784cb-117">Exempel 1: Återställ ett säkerhetskopierat certifikat</span><span class="sxs-lookup"><span data-stu-id="784cb-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="784cb-118">Det här kommandot återställer ett certifikat, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till det nyckelord som heter MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="784cb-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="784cb-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="784cb-119">PARAMETERS</span></span>

### <span data-ttu-id="784cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="784cb-120">-DefaultProfile</span></span>
<span data-ttu-id="784cb-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="784cb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="784cb-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="784cb-122">-InputFile</span></span>
<span data-ttu-id="784cb-123">Indatafil.</span><span class="sxs-lookup"><span data-stu-id="784cb-123">Input file.</span></span>
<span data-ttu-id="784cb-124">Den indatafil som innehåller den säkerhetskopierade blobben</span><span class="sxs-lookup"><span data-stu-id="784cb-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="784cb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="784cb-125">-InputObject</span></span>
<span data-ttu-id="784cb-126">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="784cb-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="784cb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="784cb-127">-ResourceId</span></span>
<span data-ttu-id="784cb-128">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="784cb-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="784cb-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="784cb-129">-VaultName</span></span>
<span data-ttu-id="784cb-130">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="784cb-130">Vault name.</span></span>
<span data-ttu-id="784cb-131">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="784cb-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="784cb-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="784cb-132">-Confirm</span></span>
<span data-ttu-id="784cb-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="784cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="784cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="784cb-134">-WhatIf</span></span>
<span data-ttu-id="784cb-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="784cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="784cb-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="784cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="784cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="784cb-137">CommonParameters</span></span>
<span data-ttu-id="784cb-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="784cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="784cb-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="784cb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="784cb-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="784cb-140">INPUTS</span></span>

### <span data-ttu-id="784cb-141">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="784cb-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="784cb-142">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="784cb-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="784cb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="784cb-143">System.String</span></span>

## <span data-ttu-id="784cb-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="784cb-144">OUTPUTS</span></span>

### <span data-ttu-id="784cb-145">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="784cb-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="784cb-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="784cb-146">NOTES</span></span>

## <span data-ttu-id="784cb-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="784cb-147">RELATED LINKS</span></span>
