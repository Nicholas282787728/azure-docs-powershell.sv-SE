---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 9fb79628b123b5d35ae5d55ba31fd07dcbd85775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916246"
---
# <span data-ttu-id="7a0a2-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a0a2-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="7a0a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0a2-103">Skapar en hemlighet i ett nyckel valv från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="7a0a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a0a2-104">SYNTAX</span></span>

### <span data-ttu-id="7a0a2-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="7a0a2-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0a2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a0a2-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0a2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a0a2-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a0a2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a0a2-108">DESCRIPTION</span></span>
<span data-ttu-id="7a0a2-109">Cmdleten **restore-AzKeyVaultSecret** skapar en hemlighet i det angivna nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="7a0a2-110">Denna hemlighet är en replik av den säkerhetskopierade hemligheten i indatafilen och har samma namn som den ursprungliga hemligheten.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="7a0a2-111">Om nyckel valvet redan har en hemlighet med samma namn, Miss lyckas denna cmdlet i stället för att skriva över den ursprungliga hemligheten.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="7a0a2-112">Om säkerhets kopian innehåller flera versioner av en hemlighet återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="7a0a2-113">Nyckel valvet som du återställer hemligheten till kan skilja sig från det nyckel valv som du säkerhetskopierade hemligheten från.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="7a0a2-114">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="7a0a2-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="7a0a2-115">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="7a0a2-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a0a2-116">EXAMPLES</span></span>

### <span data-ttu-id="7a0a2-117">Exempel 1: återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="7a0a2-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="7a0a2-118">Det här kommandot återställer en hemlighet, inklusive alla dess versioner, från säkerhets kopian som heter Backup. blob till nyckel valvet contoso.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="7a0a2-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a0a2-119">PARAMETERS</span></span>

### <span data-ttu-id="7a0a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0a2-120">-DefaultProfile</span></span>
<span data-ttu-id="7a0a2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7a0a2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a0a2-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7a0a2-122">-InputFile</span></span>
<span data-ttu-id="7a0a2-123">Anger den indatafil som innehåller säkerhets kopian av hemligheten som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="7a0a2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a0a2-124">-InputObject</span></span>
<span data-ttu-id="7a0a2-125">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="7a0a2-125">KeyVault object</span></span>

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

### <span data-ttu-id="7a0a2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a0a2-126">-ResourceId</span></span>
<span data-ttu-id="7a0a2-127">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="7a0a2-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="7a0a2-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7a0a2-128">-VaultName</span></span>
<span data-ttu-id="7a0a2-129">Anger namnet på det nyckel valv som du vill återställa hemligheten till.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="7a0a2-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7a0a2-130">-Confirm</span></span>
<span data-ttu-id="7a0a2-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0a2-132">-WhatIf</span></span>
<span data-ttu-id="7a0a2-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0a2-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0a2-135">CommonParameters</span></span>
<span data-ttu-id="7a0a2-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0a2-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0a2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0a2-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a0a2-138">INPUTS</span></span>

### <span data-ttu-id="7a0a2-139">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a0a2-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="7a0a2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7a0a2-140">System.String</span></span>

## <span data-ttu-id="7a0a2-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a0a2-141">OUTPUTS</span></span>

### <span data-ttu-id="7a0a2-142">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a0a2-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="7a0a2-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a0a2-143">NOTES</span></span>

## <span data-ttu-id="7a0a2-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a0a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="7a0a2-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a0a2-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="7a0a2-146">Säkerhets kopiering-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a0a2-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="7a0a2-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a0a2-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="7a0a2-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a0a2-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

