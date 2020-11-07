---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: e9d413a8f77422b723c2dabc57d7d68c691617d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915745"
---
# <span data-ttu-id="06f30-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="06f30-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="06f30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06f30-102">SYNOPSIS</span></span>
<span data-ttu-id="06f30-103">Synkroniserar lagrings konto nycklar för ett lagrings konto som är kopplat till medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="06f30-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="06f30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06f30-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06f30-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06f30-105">DESCRIPTION</span></span>
<span data-ttu-id="06f30-106">**AzMediaServiceStorageKey** cmdlet synkroniserar lagrings konto nycklar för ett lagrings konto som är kopplat till medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="06f30-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="06f30-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06f30-107">EXAMPLES</span></span>

### <span data-ttu-id="06f30-108">Exempel 1: synkronisera lagrings konto nycklar för ett lagrings konto som är kopplat till medie tjänsten</span><span class="sxs-lookup"><span data-stu-id="06f30-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="06f30-109">Det första kommandot använder cmdleten Get-AzStorageAccount för att hämta lagrings kontot med namnet Storage135 som tillhör ResourceGroup001 och lagrar resultatet i variabeln som heter $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="06f30-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="06f30-110">Det andra kommandot synkroniserar lagrings konto nycklar för medie tjänsten med namnet MediaService001 med egenskapen **ID** som finns i $StorageAccount variabeln.</span><span class="sxs-lookup"><span data-stu-id="06f30-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="06f30-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06f30-111">PARAMETERS</span></span>

### <span data-ttu-id="06f30-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="06f30-112">-AccountName</span></span>
<span data-ttu-id="06f30-113">Anger namnet på den medie tjänst som denna cmdlet synkroniserar.</span><span class="sxs-lookup"><span data-stu-id="06f30-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f30-114">-DefaultProfile</span></span>
<span data-ttu-id="06f30-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="06f30-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06f30-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f30-116">-ResourceGroupName</span></span>
<span data-ttu-id="06f30-117">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="06f30-117">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f30-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="06f30-118">-StorageAccountId</span></span>
<span data-ttu-id="06f30-119">Anger det lagrings konto-ID som är kopplat till medie tjänstens konto.</span><span class="sxs-lookup"><span data-stu-id="06f30-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06f30-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06f30-120">-Confirm</span></span>
<span data-ttu-id="06f30-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06f30-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f30-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f30-122">-WhatIf</span></span>
<span data-ttu-id="06f30-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06f30-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f30-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06f30-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f30-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f30-125">CommonParameters</span></span>
<span data-ttu-id="06f30-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f30-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f30-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06f30-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f30-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06f30-128">INPUTS</span></span>

### <span data-ttu-id="06f30-129">System. String</span><span class="sxs-lookup"><span data-stu-id="06f30-129">System.String</span></span>

## <span data-ttu-id="06f30-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06f30-130">OUTPUTS</span></span>

### <span data-ttu-id="06f30-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06f30-131">System.Boolean</span></span>

## <span data-ttu-id="06f30-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06f30-132">NOTES</span></span>

## <span data-ttu-id="06f30-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06f30-133">RELATED LINKS</span></span>
