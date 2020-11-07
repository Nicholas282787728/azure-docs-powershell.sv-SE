---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 6cef357b636a48e433d545a56d2b5105556842da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758045"
---
# <span data-ttu-id="39b19-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="39b19-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="39b19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39b19-102">SYNOPSIS</span></span>
<span data-ttu-id="39b19-103">Hämtar viktig information för åtkomst till den REST-slutpunkt som är associerad med medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="39b19-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39b19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39b19-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39b19-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39b19-105">DESCRIPTION</span></span>
<span data-ttu-id="39b19-106">Cmdleten **Get-AzureRmMediaServiceKeys** hämtar viktig information för att få åtkomst till den ompresentations status överföring (rest) som är associerad med Azure Media-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="39b19-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="39b19-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39b19-107">EXAMPLES</span></span>

### <span data-ttu-id="39b19-108">Exempel 1: Hämta viktig information för att komma åt medie tjänsten</span><span class="sxs-lookup"><span data-stu-id="39b19-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="39b19-109">Det här kommandot får viktig information för åtkomst till medie tjänsten med namnet MediaService001 som tillhör resurs gruppen med namnet ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="39b19-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="39b19-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39b19-110">PARAMETERS</span></span>

### <span data-ttu-id="39b19-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39b19-111">-AccountName</span></span>
<span data-ttu-id="39b19-112">Anger namnet på den medie tjänst som denna cmdlet hämtar medie tjänstens nycklar från.</span><span class="sxs-lookup"><span data-stu-id="39b19-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="39b19-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39b19-113">-ResourceGroupName</span></span>
<span data-ttu-id="39b19-114">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="39b19-114">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="39b19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b19-115">-DefaultProfile</span></span>
<span data-ttu-id="39b19-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39b19-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39b19-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b19-117">CommonParameters</span></span>
<span data-ttu-id="39b19-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39b19-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b19-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39b19-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b19-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39b19-120">INPUTS</span></span>

## <span data-ttu-id="39b19-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39b19-121">OUTPUTS</span></span>

### <span data-ttu-id="39b19-122">Microsoft. Azure. commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="39b19-122">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="39b19-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39b19-123">NOTES</span></span>

## <span data-ttu-id="39b19-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39b19-124">RELATED LINKS</span></span>

[<span data-ttu-id="39b19-125">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="39b19-125">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


