---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: b96c8717e20395c57e6c9d5d4520327d97dfa174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576507"
---
# <span data-ttu-id="c7729-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c7729-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="c7729-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7729-102">SYNOPSIS</span></span>
<span data-ttu-id="c7729-103">Hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="c7729-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7729-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7729-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7729-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7729-105">DESCRIPTION</span></span>
<span data-ttu-id="c7729-106">Cmdleten **Get-AzureRmLogProfile** hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="c7729-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="c7729-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7729-107">EXAMPLES</span></span>

## <span data-ttu-id="c7729-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7729-108">PARAMETERS</span></span>

### <span data-ttu-id="c7729-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7729-109">-DefaultProfile</span></span>
<span data-ttu-id="c7729-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c7729-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7729-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7729-111">-Name</span></span>
<span data-ttu-id="c7729-112">Anger namnet på den logg profil som ska visas.</span><span class="sxs-lookup"><span data-stu-id="c7729-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7729-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7729-113">CommonParameters</span></span>
<span data-ttu-id="c7729-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7729-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7729-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7729-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7729-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7729-116">INPUTS</span></span>

### <span data-ttu-id="c7729-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="c7729-117">None</span></span>
<span data-ttu-id="c7729-118">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c7729-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7729-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7729-119">OUTPUTS</span></span>

### <span data-ttu-id="c7729-120">Microsoft. Azure. commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="c7729-120">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="c7729-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7729-121">NOTES</span></span>

## <span data-ttu-id="c7729-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7729-122">RELATED LINKS</span></span>

[<span data-ttu-id="c7729-123">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c7729-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="c7729-124">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c7729-124">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


