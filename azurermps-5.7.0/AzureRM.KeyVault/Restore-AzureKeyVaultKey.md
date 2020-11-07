---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: aee61173ee327d0c65f4cc04451fd64f51a79522
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756084"
---
# <span data-ttu-id="225d4-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="225d4-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="225d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="225d4-102">SYNOPSIS</span></span>
<span data-ttu-id="225d4-103">Skapar en nycklar i ett nyckelord från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="225d4-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="225d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="225d4-104">SYNTAX</span></span>

### <span data-ttu-id="225d4-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="225d4-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="225d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="225d4-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="225d4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="225d4-107">DESCRIPTION</span></span>
<span data-ttu-id="225d4-108">Cmdleten **restore-AzureKeyVaultKey** skapar en Key i det angivna nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="225d4-108">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="225d4-109">Den här tangenten är en replik av säkerhets kopian i indatafilen och har samma namn som den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="225d4-109">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="225d4-110">Om det redan finns en nycklar med samma namn i nyckelordet kan denna cmdlet inte skriva över den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="225d4-110">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="225d4-111">Om säkerhets kopian innehåller flera versioner av en, återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="225d4-111">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="225d4-112">Huvud valvet som du återställer nycklar till kan skilja sig från det viktiga valv som du säkerhetskopierade från.</span><span class="sxs-lookup"><span data-stu-id="225d4-112">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="225d4-113">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="225d4-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="225d4-114">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="225d4-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="225d4-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="225d4-115">EXAMPLES</span></span>

### <span data-ttu-id="225d4-116">Exempel 1: återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="225d4-116">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="225d4-117">Det här kommandot återställer en nycklar, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till det nyckelord som heter MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="225d4-117">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="225d4-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="225d4-118">PARAMETERS</span></span>

### <span data-ttu-id="225d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225d4-119">-DefaultProfile</span></span>
<span data-ttu-id="225d4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="225d4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="225d4-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="225d4-121">-InputFile</span></span>
<span data-ttu-id="225d4-122">Anger den indatafil som innehåller säkerhets kopian av den fil som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="225d4-122">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="225d4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="225d4-123">-InputObject</span></span>
<span data-ttu-id="225d4-124">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="225d4-124">KeyVault object</span></span>

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

### <span data-ttu-id="225d4-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="225d4-125">-VaultName</span></span>
<span data-ttu-id="225d4-126">Anger namnet på det nyckelord som du vill återställa.</span><span class="sxs-lookup"><span data-stu-id="225d4-126">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="225d4-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="225d4-127">-Confirm</span></span>
<span data-ttu-id="225d4-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="225d4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="225d4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="225d4-129">-WhatIf</span></span>
<span data-ttu-id="225d4-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="225d4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="225d4-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="225d4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="225d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225d4-132">CommonParameters</span></span>
<span data-ttu-id="225d4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="225d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225d4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="225d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225d4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="225d4-135">INPUTS</span></span>

### <span data-ttu-id="225d4-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="225d4-136">None</span></span>
<span data-ttu-id="225d4-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="225d4-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="225d4-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="225d4-138">OUTPUTS</span></span>

### <span data-ttu-id="225d4-139">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="225d4-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="225d4-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="225d4-140">NOTES</span></span>

## <span data-ttu-id="225d4-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="225d4-141">RELATED LINKS</span></span>

[<span data-ttu-id="225d4-142">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="225d4-142">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="225d4-143">Säkerhets kopiering-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="225d4-143">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="225d4-144">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="225d4-144">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="225d4-145">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="225d4-145">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

