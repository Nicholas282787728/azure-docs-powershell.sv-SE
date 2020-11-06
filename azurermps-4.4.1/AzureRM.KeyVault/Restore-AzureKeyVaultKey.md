---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 1fb58d348af5f507e1bd3c8451f12918c69b309b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585492"
---
# <span data-ttu-id="8532a-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8532a-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="8532a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8532a-102">SYNOPSIS</span></span>
<span data-ttu-id="8532a-103">Skapar en nycklar i ett nyckelord från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="8532a-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8532a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8532a-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8532a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8532a-105">DESCRIPTION</span></span>
<span data-ttu-id="8532a-106">Cmdleten **restore-AzureKeyVaultKey** skapar en Key i det angivna nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="8532a-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="8532a-107">Den här tangenten är en replik av säkerhets kopian i indatafilen och har samma namn som den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="8532a-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="8532a-108">Om det redan finns en nycklar med samma namn i nyckelordet kan denna cmdlet inte skriva över den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="8532a-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="8532a-109">Om säkerhets kopian innehåller flera versioner av en, återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="8532a-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="8532a-110">Huvud valvet som du återställer nycklar till kan skilja sig från det viktiga valv som du säkerhetskopierade från.</span><span class="sxs-lookup"><span data-stu-id="8532a-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="8532a-111">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="8532a-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="8532a-112">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="8532a-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="8532a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8532a-113">EXAMPLES</span></span>

### <span data-ttu-id="8532a-114">Exempel 1: återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="8532a-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="8532a-115">Det här kommandot återställer en nycklar, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till det nyckelord som heter MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8532a-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="8532a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8532a-116">PARAMETERS</span></span>

### <span data-ttu-id="8532a-117">-InputFile</span><span class="sxs-lookup"><span data-stu-id="8532a-117">-InputFile</span></span>
<span data-ttu-id="8532a-118">Anger den indatafil som innehåller säkerhets kopian av den fil som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="8532a-118">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8532a-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8532a-119">-VaultName</span></span>
<span data-ttu-id="8532a-120">Anger namnet på det nyckelord som du vill återställa.</span><span class="sxs-lookup"><span data-stu-id="8532a-120">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8532a-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8532a-121">-Confirm</span></span>
<span data-ttu-id="8532a-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8532a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8532a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8532a-123">-WhatIf</span></span>
<span data-ttu-id="8532a-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8532a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8532a-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8532a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8532a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8532a-126">-DefaultProfile</span></span>
<span data-ttu-id="8532a-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8532a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8532a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8532a-128">CommonParameters</span></span>
<span data-ttu-id="8532a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8532a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8532a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8532a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8532a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8532a-131">INPUTS</span></span>

## <span data-ttu-id="8532a-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8532a-132">OUTPUTS</span></span>

### <span data-ttu-id="8532a-133">Microsoft. Azure. commands...</span><span class="sxs-lookup"><span data-stu-id="8532a-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="8532a-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8532a-134">NOTES</span></span>

## <span data-ttu-id="8532a-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8532a-135">RELATED LINKS</span></span>

[<span data-ttu-id="8532a-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8532a-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="8532a-137">Säkerhets kopiering-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8532a-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="8532a-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8532a-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="8532a-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8532a-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

