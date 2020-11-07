---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 4691d37532db3dd8e629bf1daad2654558a31de3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924457"
---
# <span data-ttu-id="b9827-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b9827-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="b9827-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9827-102">SYNOPSIS</span></span>
<span data-ttu-id="b9827-103">Skapar en hemlighet i ett nyckel valv från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="b9827-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="b9827-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9827-104">SYNTAX</span></span>

```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9827-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9827-105">DESCRIPTION</span></span>
<span data-ttu-id="b9827-106">Cmdleten **restore-AzKeyVaultSecret** skapar en hemlighet i det angivna nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="b9827-106">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="b9827-107">Denna hemlighet är en replik av den säkerhetskopierade hemligheten i indatafilen och har samma namn som den ursprungliga hemligheten.</span><span class="sxs-lookup"><span data-stu-id="b9827-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="b9827-108">Om nyckel valvet redan har en hemlighet med samma namn, Miss lyckas denna cmdlet i stället för att skriva över den ursprungliga hemligheten.</span><span class="sxs-lookup"><span data-stu-id="b9827-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="b9827-109">Om säkerhets kopian innehåller flera versioner av en hemlighet återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="b9827-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="b9827-110">Nyckel valvet som du återställer hemligheten till kan skilja sig från det nyckel valv som du säkerhetskopierade hemligheten från.</span><span class="sxs-lookup"><span data-stu-id="b9827-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="b9827-111">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="b9827-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="b9827-112">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="b9827-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="b9827-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9827-113">EXAMPLES</span></span>

### <span data-ttu-id="b9827-114">Exempel 1: återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="b9827-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="b9827-115">Det här kommandot återställer en hemlighet, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till nyckel valvet med namnet MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="b9827-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="b9827-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9827-116">PARAMETERS</span></span>

### <span data-ttu-id="b9827-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9827-117">-DefaultProfile</span></span>
<span data-ttu-id="b9827-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b9827-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9827-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b9827-119">-InputFile</span></span>
<span data-ttu-id="b9827-120">Anger den indatafil som innehåller säkerhets kopian av hemligheten som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="b9827-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="b9827-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b9827-121">-VaultName</span></span>
<span data-ttu-id="b9827-122">Anger namnet på det nyckel valv som du vill återställa hemligheten till.</span><span class="sxs-lookup"><span data-stu-id="b9827-122">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9827-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9827-123">-Confirm</span></span>
<span data-ttu-id="b9827-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9827-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9827-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9827-125">-WhatIf</span></span>
<span data-ttu-id="b9827-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9827-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9827-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9827-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9827-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9827-128">CommonParameters</span></span>
<span data-ttu-id="b9827-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9827-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9827-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9827-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9827-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9827-131">INPUTS</span></span>

### <span data-ttu-id="b9827-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="b9827-132">None</span></span>
<span data-ttu-id="b9827-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b9827-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9827-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9827-134">OUTPUTS</span></span>

### <span data-ttu-id="b9827-135">Microsoft. Azure. commands. nyckel valv. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="b9827-135">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="b9827-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9827-136">NOTES</span></span>

## <span data-ttu-id="b9827-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9827-137">RELATED LINKS</span></span>

[<span data-ttu-id="b9827-138">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b9827-138">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="b9827-139">Säkerhets kopiering-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b9827-139">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="b9827-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b9827-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="b9827-141">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b9827-141">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

