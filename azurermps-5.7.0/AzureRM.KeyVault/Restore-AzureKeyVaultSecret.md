---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: 1ba12a18c88004dcc1c6761d71fdc1983a5ba0c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579516"
---
# <span data-ttu-id="78921-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78921-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="78921-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78921-102">SYNOPSIS</span></span>
<span data-ttu-id="78921-103">Skapar en hemlighet i ett nyckel valv från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="78921-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78921-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78921-104">SYNTAX</span></span>

### <span data-ttu-id="78921-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="78921-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78921-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78921-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78921-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78921-107">DESCRIPTION</span></span>
<span data-ttu-id="78921-108">Cmdleten **restore-AzureKeyVaultSecret** skapar en hemlighet i det angivna nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="78921-108">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="78921-109">Denna hemlighet är en replik av den säkerhetskopierade hemligheten i indatafilen och har samma namn som den ursprungliga hemligheten.</span><span class="sxs-lookup"><span data-stu-id="78921-109">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="78921-110">Om nyckel valvet redan har en hemlighet med samma namn, Miss lyckas denna cmdlet i stället för att skriva över den ursprungliga hemligheten.</span><span class="sxs-lookup"><span data-stu-id="78921-110">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="78921-111">Om säkerhets kopian innehåller flera versioner av en hemlighet återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="78921-111">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="78921-112">Nyckel valvet som du återställer hemligheten till kan skilja sig från det nyckel valv som du säkerhetskopierade hemligheten från.</span><span class="sxs-lookup"><span data-stu-id="78921-112">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="78921-113">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="78921-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="78921-114">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="78921-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="78921-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78921-115">EXAMPLES</span></span>

### <span data-ttu-id="78921-116">Exempel 1: återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="78921-116">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="78921-117">Det här kommandot återställer en hemlighet, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till nyckel valvet med namnet MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="78921-117">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="78921-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78921-118">PARAMETERS</span></span>

### <span data-ttu-id="78921-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78921-119">-DefaultProfile</span></span>
<span data-ttu-id="78921-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="78921-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78921-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="78921-121">-InputFile</span></span>
<span data-ttu-id="78921-122">Anger den indatafil som innehåller säkerhets kopian av hemligheten som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="78921-122">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78921-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78921-123">-InputObject</span></span>
<span data-ttu-id="78921-124">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="78921-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78921-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="78921-125">-VaultName</span></span>
<span data-ttu-id="78921-126">Anger namnet på det nyckel valv som du vill återställa hemligheten till.</span><span class="sxs-lookup"><span data-stu-id="78921-126">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78921-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="78921-127">-Confirm</span></span>
<span data-ttu-id="78921-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="78921-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78921-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78921-129">-WhatIf</span></span>
<span data-ttu-id="78921-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="78921-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78921-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="78921-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78921-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78921-132">CommonParameters</span></span>
<span data-ttu-id="78921-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78921-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78921-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78921-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78921-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78921-135">INPUTS</span></span>

### <span data-ttu-id="78921-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="78921-136">None</span></span>
<span data-ttu-id="78921-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="78921-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78921-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78921-138">OUTPUTS</span></span>

### <span data-ttu-id="78921-139">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78921-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="78921-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78921-140">NOTES</span></span>

## <span data-ttu-id="78921-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78921-141">RELATED LINKS</span></span>

[<span data-ttu-id="78921-142">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78921-142">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="78921-143">Säkerhets kopiering-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78921-143">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="78921-144">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78921-144">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="78921-145">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="78921-145">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

