---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522594"
---
# <span data-ttu-id="96be1-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="96be1-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="96be1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96be1-102">SYNOPSIS</span></span>
<span data-ttu-id="96be1-103">Återställer ett certifikat i ett nyckelord från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="96be1-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="96be1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96be1-104">SYNTAX</span></span>

### <span data-ttu-id="96be1-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="96be1-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96be1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="96be1-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96be1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="96be1-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96be1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96be1-108">DESCRIPTION</span></span>
<span data-ttu-id="96be1-109">Cmdleten **restore-AzKeyVaultCertificate** skapar ett certifikat i det angivna nyckelvärdet från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="96be1-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="96be1-110">Det här certifikatet är en replik av säkerhetskopierat certifikat i indatafilen och har samma namn som det ursprungliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="96be1-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="96be1-111">Om det redan finns ett certifikat med samma namn i huvud valvet Miss lyckas denna cmdlet i stället för att skriva över det ursprungliga certifikatet.</span><span class="sxs-lookup"><span data-stu-id="96be1-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="96be1-112">Om säkerhets kopian innehåller flera versioner av ett certifikat återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="96be1-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="96be1-113">Det viktigaste valvet du återställer certifikatet till kan skilja sig från det huvud valv som du säkerhetskopierade certifikatet från.</span><span class="sxs-lookup"><span data-stu-id="96be1-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="96be1-114">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="96be1-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="96be1-115">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="96be1-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="96be1-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96be1-116">EXAMPLES</span></span>

### <span data-ttu-id="96be1-117">Exempel 1: Återställ ett säkerhetskopierat certifikat</span><span class="sxs-lookup"><span data-stu-id="96be1-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="96be1-118">Det här kommandot återställer ett certifikat, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till det nyckelord som heter MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="96be1-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="96be1-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96be1-119">PARAMETERS</span></span>

### <span data-ttu-id="96be1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96be1-120">-DefaultProfile</span></span>
<span data-ttu-id="96be1-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96be1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96be1-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="96be1-122">-InputFile</span></span>
<span data-ttu-id="96be1-123">Indatafil.</span><span class="sxs-lookup"><span data-stu-id="96be1-123">Input file.</span></span>
<span data-ttu-id="96be1-124">Den indatafil som innehåller den säkerhetskopierade blobben</span><span class="sxs-lookup"><span data-stu-id="96be1-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="96be1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96be1-125">-InputObject</span></span>
<span data-ttu-id="96be1-126">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="96be1-126">KeyVault object</span></span>

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

### <span data-ttu-id="96be1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96be1-127">-ResourceId</span></span>
<span data-ttu-id="96be1-128">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="96be1-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="96be1-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="96be1-129">-VaultName</span></span>
<span data-ttu-id="96be1-130">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="96be1-130">Vault name.</span></span>
<span data-ttu-id="96be1-131">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="96be1-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="96be1-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="96be1-132">-Confirm</span></span>
<span data-ttu-id="96be1-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="96be1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96be1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96be1-134">-WhatIf</span></span>
<span data-ttu-id="96be1-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="96be1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96be1-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="96be1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96be1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96be1-137">CommonParameters</span></span>
<span data-ttu-id="96be1-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96be1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96be1-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96be1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96be1-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96be1-140">INPUTS</span></span>

### <span data-ttu-id="96be1-141">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="96be1-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="96be1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="96be1-142">System.String</span></span>

## <span data-ttu-id="96be1-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96be1-143">OUTPUTS</span></span>

### <span data-ttu-id="96be1-144">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="96be1-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="96be1-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96be1-145">NOTES</span></span>

## <span data-ttu-id="96be1-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96be1-146">RELATED LINKS</span></span>
