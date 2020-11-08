---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093407"
---
# <span data-ttu-id="ae31b-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ae31b-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="ae31b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae31b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae31b-103">Exporterar mal len för en Azure RemoteApp-samling till det angivna Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="ae31b-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="ae31b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae31b-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae31b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae31b-105">DESCRIPTION</span></span>
<span data-ttu-id="ae31b-106">Cmdleten **export-AzureRemoteAppTemplateImage** exporterar mallen för en Azure RemoteApp till det angivna Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="ae31b-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="ae31b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae31b-107">EXAMPLES</span></span>

### <span data-ttu-id="ae31b-108">Exempel 1: exportera en mall till Azure Storage-kontot</span><span class="sxs-lookup"><span data-stu-id="ae31b-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="ae31b-109">Det här kommandot exporterar mal len för samlingen med namnet contoso till en container med namnet ContainerName i det angivna Azure Storage-kontot med namn AccountName och Key AccountKey.</span><span class="sxs-lookup"><span data-stu-id="ae31b-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="ae31b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae31b-110">PARAMETERS</span></span>

### <span data-ttu-id="ae31b-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="ae31b-111">-CollectionName</span></span>
<span data-ttu-id="ae31b-112">Anger namnet på käll-Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="ae31b-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae31b-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="ae31b-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="ae31b-114">Anger namnet på en behållare i mål Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="ae31b-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae31b-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ae31b-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="ae31b-116">Anger tangenten för mål Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="ae31b-116">Specifies the key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae31b-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae31b-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="ae31b-118">Anger namnet på mål Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="ae31b-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae31b-119">-OverwriteExistingTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ae31b-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="ae31b-120">Anger att cmdleten skriver över den befintliga mallen.</span><span class="sxs-lookup"><span data-stu-id="ae31b-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae31b-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="ae31b-121">-Profile</span></span>
<span data-ttu-id="ae31b-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ae31b-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae31b-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ae31b-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae31b-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae31b-124">-Confirm</span></span>
<span data-ttu-id="ae31b-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae31b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae31b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae31b-126">-WhatIf</span></span>
<span data-ttu-id="ae31b-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae31b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae31b-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae31b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae31b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae31b-129">CommonParameters</span></span>
<span data-ttu-id="ae31b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae31b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae31b-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae31b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae31b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae31b-132">INPUTS</span></span>

## <span data-ttu-id="ae31b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae31b-133">OUTPUTS</span></span>

## <span data-ttu-id="ae31b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae31b-134">NOTES</span></span>

## <span data-ttu-id="ae31b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae31b-135">RELATED LINKS</span></span>

[<span data-ttu-id="ae31b-136">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ae31b-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="ae31b-137">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ae31b-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="ae31b-138">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ae31b-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="ae31b-139">Rename – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ae31b-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


