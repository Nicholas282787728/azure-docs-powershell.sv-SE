---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 72D332BA-A30B-45B9-875C-DF9D33299E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ddfbdc7da2f398ae1db11cf87de344c4f4ed5de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093404"
---
# <span data-ttu-id="6653f-101">Export-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="6653f-101">Export-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="6653f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6653f-102">SYNOPSIS</span></span>
<span data-ttu-id="6653f-103">Exporterar alla användar diskar från en Azure RemoteApp-samling till det angivna Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="6653f-103">Exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="6653f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6653f-104">SYNTAX</span></span>

```
Export-AzureRemoteAppUserDisk [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6653f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6653f-105">DESCRIPTION</span></span>
<span data-ttu-id="6653f-106">Cmdleten **export-AzureRemoteAppUserDisk** exporterar alla användar diskar från en Azure RemoteApp-samling till det angivna Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="6653f-106">The **Export-AzureRemoteAppUserDisk** cmdlet exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="6653f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6653f-107">EXAMPLES</span></span>

### <span data-ttu-id="6653f-108">Exempel 1: exportera alla användar diskar från en samling till det angivna Azure Storage-kontot</span><span class="sxs-lookup"><span data-stu-id="6653f-108">Example 1: Export all the user disks from a collection to the specified Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppUserDisk -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingUserDisk
```

<span data-ttu-id="6653f-109">Det här kommandot exporterar alla användar diskar från samlingen med namnet contoso till en container med namnet ContainerName i det angivna Azure Storage-kontot med namn AccountName och Key AccountKey.</span><span class="sxs-lookup"><span data-stu-id="6653f-109">This command exports all the user disks from the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="6653f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6653f-110">PARAMETERS</span></span>

### <span data-ttu-id="6653f-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="6653f-111">-CollectionName</span></span>
<span data-ttu-id="6653f-112">Anger namnet på käll-Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="6653f-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="6653f-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="6653f-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="6653f-114">Anger namnet på en behållare i mål Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="6653f-114">Specifies the name of a container in the destination Azure storage account.</span></span>

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

### <span data-ttu-id="6653f-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6653f-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="6653f-116">Anger tangenten för mål Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="6653f-116">Specifies the Key of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="6653f-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6653f-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="6653f-118">Anger namnet på mål Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="6653f-118">Specifies the name of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="6653f-119">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="6653f-119">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="6653f-120">Anger att cmdleten skriver över befintlig användar disk.</span><span class="sxs-lookup"><span data-stu-id="6653f-120">Indicates that the cmdlet overwrites the existing user disk.</span></span>

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

### <span data-ttu-id="6653f-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6653f-121">-Profile</span></span>
<span data-ttu-id="6653f-122">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6653f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6653f-123">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6653f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6653f-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6653f-124">-Confirm</span></span>
<span data-ttu-id="6653f-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6653f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6653f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6653f-126">-WhatIf</span></span>
<span data-ttu-id="6653f-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6653f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6653f-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6653f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6653f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6653f-129">CommonParameters</span></span>
<span data-ttu-id="6653f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6653f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6653f-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6653f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6653f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6653f-132">INPUTS</span></span>

## <span data-ttu-id="6653f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6653f-133">OUTPUTS</span></span>

## <span data-ttu-id="6653f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6653f-134">NOTES</span></span>

## <span data-ttu-id="6653f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6653f-135">RELATED LINKS</span></span>

[<span data-ttu-id="6653f-136">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="6653f-136">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)

[<span data-ttu-id="6653f-137">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="6653f-137">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


