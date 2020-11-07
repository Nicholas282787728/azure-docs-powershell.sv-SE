---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 8b1f4a10ab974f50a01ba0725285ccd7a3b7dffc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756273"
---
# <span data-ttu-id="50ec1-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="50ec1-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="50ec1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="50ec1-103">Hämtar information om en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="50ec1-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50ec1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50ec1-104">SYNTAX</span></span>

### <span data-ttu-id="50ec1-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="50ec1-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50ec1-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50ec1-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50ec1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50ec1-107">DESCRIPTION</span></span>
<span data-ttu-id="50ec1-108">Cmdleten **Get-AzureRmMediaService** hämtar information om en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="50ec1-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="50ec1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50ec1-109">EXAMPLES</span></span>

### <span data-ttu-id="50ec1-110">Exempel 1: Hämta alla medie tjänster i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="50ec1-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="50ec1-111">Det här kommandot får egenskaper för alla medie tjänster i resurs gruppen som heter ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="50ec1-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="50ec1-112">Exempel 2: Hämta egenskaper för medie tjänster</span><span class="sxs-lookup"><span data-stu-id="50ec1-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="50ec1-113">Det här kommandot får egenskaperna för medie tjänsten som heter MediaService1 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="50ec1-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="50ec1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50ec1-114">PARAMETERS</span></span>

### <span data-ttu-id="50ec1-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="50ec1-115">-AccountName</span></span>
<span data-ttu-id="50ec1-116">Anger namnet på den medie tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="50ec1-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50ec1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ec1-117">-DefaultProfile</span></span>
<span data-ttu-id="50ec1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="50ec1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50ec1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50ec1-119">-ResourceGroupName</span></span>
<span data-ttu-id="50ec1-120">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="50ec1-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="50ec1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ec1-121">CommonParameters</span></span>
<span data-ttu-id="50ec1-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ec1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ec1-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50ec1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ec1-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50ec1-124">INPUTS</span></span>

### <span data-ttu-id="50ec1-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="50ec1-125">None</span></span>
<span data-ttu-id="50ec1-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="50ec1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="50ec1-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50ec1-127">OUTPUTS</span></span>

### <span data-ttu-id="50ec1-128">Microsoft. Azure. commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="50ec1-128">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="50ec1-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50ec1-129">NOTES</span></span>

## <span data-ttu-id="50ec1-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50ec1-130">RELATED LINKS</span></span>

[<span data-ttu-id="50ec1-131">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="50ec1-131">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="50ec1-132">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="50ec1-132">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="50ec1-133">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="50ec1-133">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


