---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 5d090bae05e3d931fbf41b656ea66409d1297e8f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924462"
---
# <span data-ttu-id="57471-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57471-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="57471-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57471-102">SYNOPSIS</span></span>
<span data-ttu-id="57471-103">Skapar en nycklar i ett nyckelord från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="57471-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="57471-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57471-104">SYNTAX</span></span>

```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57471-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57471-105">DESCRIPTION</span></span>
<span data-ttu-id="57471-106">Cmdleten **restore-AzKeyVaultKey** skapar en Key i det angivna nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="57471-106">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="57471-107">Den här tangenten är en replik av säkerhets kopian i indatafilen och har samma namn som den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="57471-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="57471-108">Om det redan finns en nycklar med samma namn i nyckelordet kan denna cmdlet inte skriva över den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="57471-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="57471-109">Om säkerhets kopian innehåller flera versioner av en, återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="57471-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="57471-110">Huvud valvet som du återställer nycklar till kan skilja sig från det viktiga valv som du säkerhetskopierade från.</span><span class="sxs-lookup"><span data-stu-id="57471-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="57471-111">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="57471-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="57471-112">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="57471-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="57471-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57471-113">EXAMPLES</span></span>

### <span data-ttu-id="57471-114">Exempel 1: återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="57471-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="57471-115">Det här kommandot återställer en nycklar, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till det nyckelord som heter MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="57471-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="57471-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57471-116">PARAMETERS</span></span>

### <span data-ttu-id="57471-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57471-117">-DefaultProfile</span></span>
<span data-ttu-id="57471-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="57471-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57471-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="57471-119">-InputFile</span></span>
<span data-ttu-id="57471-120">Anger den indatafil som innehåller säkerhets kopian av den fil som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="57471-120">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="57471-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="57471-121">-VaultName</span></span>
<span data-ttu-id="57471-122">Anger namnet på det nyckelord som du vill återställa.</span><span class="sxs-lookup"><span data-stu-id="57471-122">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="57471-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57471-123">-Confirm</span></span>
<span data-ttu-id="57471-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57471-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57471-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57471-125">-WhatIf</span></span>
<span data-ttu-id="57471-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57471-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57471-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57471-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57471-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57471-128">CommonParameters</span></span>
<span data-ttu-id="57471-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57471-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57471-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57471-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57471-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57471-131">INPUTS</span></span>

### <span data-ttu-id="57471-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="57471-132">None</span></span>
<span data-ttu-id="57471-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="57471-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57471-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57471-134">OUTPUTS</span></span>

### <span data-ttu-id="57471-135">Microsoft. Azure. commands...</span><span class="sxs-lookup"><span data-stu-id="57471-135">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="57471-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57471-136">NOTES</span></span>

## <span data-ttu-id="57471-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57471-137">RELATED LINKS</span></span>

[<span data-ttu-id="57471-138">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57471-138">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="57471-139">Säkerhets kopiering-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57471-139">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="57471-140">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57471-140">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="57471-141">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57471-141">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

