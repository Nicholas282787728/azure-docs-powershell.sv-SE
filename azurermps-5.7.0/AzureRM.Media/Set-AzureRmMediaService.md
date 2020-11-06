---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 413a357d793bd72ff7d1e30cb65e56cb5bd5f3a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577179"
---
# <span data-ttu-id="3cfc4-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3cfc4-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="3cfc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3cfc4-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfc4-103">Ändrar angivna egenskaper för en befintlig medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cfc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3cfc4-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cfc4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3cfc4-105">DESCRIPTION</span></span>
<span data-ttu-id="3cfc4-106">Cmdleten **set-AzureRmMediaService** ändrar angivna egenskaper för en befintlig medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="3cfc4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3cfc4-107">EXAMPLES</span></span>

### <span data-ttu-id="3cfc4-108">Exempel 1: ändra en befintlig medie tjänst</span><span class="sxs-lookup"><span data-stu-id="3cfc4-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="3cfc4-109">Det första kommandot skapar en serie Taggar och lagrar taggarna i variabeln som heter $Tags.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>

<span data-ttu-id="3cfc4-110">Det här andra kommandot uppdaterar medie tjänsten med namnet MediaService001 som tillhör resurs gruppen med namnet ResourceGroup123 med taggarna i $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="3cfc4-111">Kommandot använder också en matris med lagrings konfigurations objekt som lagras i $StorageAccounts variabel.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="3cfc4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3cfc4-112">PARAMETERS</span></span>

### <span data-ttu-id="3cfc4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3cfc4-113">-AccountName</span></span>
<span data-ttu-id="3cfc4-114">Anger namnet på den medie tjänst som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cfc4-115">-DefaultProfile</span></span>
<span data-ttu-id="3cfc4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3cfc4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cfc4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cfc4-117">-ResourceGroupName</span></span>
<span data-ttu-id="3cfc4-118">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="3cfc4-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3cfc4-119">-StorageAccounts</span></span>
<span data-ttu-id="3cfc4-120">Anger en matris med lagrings konton som denna cmdlet associerar med medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfc4-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3cfc4-121">-Tag</span></span>
<span data-ttu-id="3cfc4-122">De taggar som är kopplade till medie kontot.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-122">The tags associated with the media account.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfc4-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3cfc4-123">-Confirm</span></span>
<span data-ttu-id="3cfc4-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cfc4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cfc4-125">-WhatIf</span></span>
<span data-ttu-id="3cfc4-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cfc4-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cfc4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfc4-128">CommonParameters</span></span>
<span data-ttu-id="3cfc4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfc4-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cfc4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfc4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3cfc4-131">INPUTS</span></span>

### <span data-ttu-id="3cfc4-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="3cfc4-132">None</span></span>
<span data-ttu-id="3cfc4-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3cfc4-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3cfc4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3cfc4-134">OUTPUTS</span></span>

### <span data-ttu-id="3cfc4-135">Microsoft. Azure. commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="3cfc4-135">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="3cfc4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3cfc4-136">NOTES</span></span>

## <span data-ttu-id="3cfc4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3cfc4-137">RELATED LINKS</span></span>

[<span data-ttu-id="3cfc4-138">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3cfc4-138">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="3cfc4-139">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3cfc4-139">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="3cfc4-140">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3cfc4-140">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


