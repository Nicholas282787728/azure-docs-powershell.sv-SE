---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 76705a699b814bf52d7c874ec86e067735764936
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576248"
---
# <span data-ttu-id="84485-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="84485-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="84485-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84485-102">SYNOPSIS</span></span>
<span data-ttu-id="84485-103">Hämtar information om en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="84485-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84485-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84485-104">SYNTAX</span></span>

### <span data-ttu-id="84485-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="84485-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84485-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84485-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84485-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84485-107">DESCRIPTION</span></span>
<span data-ttu-id="84485-108">Cmdleten **Get-AzureRmMediaService** hämtar information om en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="84485-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="84485-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84485-109">EXAMPLES</span></span>

### <span data-ttu-id="84485-110">Exempel 1: Hämta alla medie tjänster i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="84485-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="84485-111">Det här kommandot får egenskaper för alla medie tjänster i resurs gruppen som heter ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="84485-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="84485-112">Exempel 2: Hämta egenskaper för medie tjänster</span><span class="sxs-lookup"><span data-stu-id="84485-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="84485-113">Det här kommandot får egenskaperna för medie tjänsten som heter MediaService1 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="84485-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="84485-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84485-114">PARAMETERS</span></span>

### <span data-ttu-id="84485-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="84485-115">-AccountName</span></span>
<span data-ttu-id="84485-116">Anger namnet på den medie tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="84485-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84485-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84485-117">-DefaultProfile</span></span>
<span data-ttu-id="84485-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="84485-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84485-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84485-119">-ResourceGroupName</span></span>
<span data-ttu-id="84485-120">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="84485-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="84485-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84485-121">CommonParameters</span></span>
<span data-ttu-id="84485-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84485-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84485-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84485-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84485-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84485-124">INPUTS</span></span>

### <span data-ttu-id="84485-125">System. String</span><span class="sxs-lookup"><span data-stu-id="84485-125">System.String</span></span>

## <span data-ttu-id="84485-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84485-126">OUTPUTS</span></span>

### <span data-ttu-id="84485-127">Microsoft. Azure. commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="84485-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="84485-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84485-128">NOTES</span></span>

## <span data-ttu-id="84485-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84485-129">RELATED LINKS</span></span>

[<span data-ttu-id="84485-130">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="84485-130">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="84485-131">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="84485-131">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="84485-132">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="84485-132">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)

