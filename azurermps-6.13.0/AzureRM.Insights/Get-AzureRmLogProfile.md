---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: d6ee5a3acfd2cfafb66f0517f21f087b7a8550e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585000"
---
# <span data-ttu-id="99dbf-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="99dbf-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="99dbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="99dbf-103">Hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="99dbf-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99dbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99dbf-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99dbf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="99dbf-106">Cmdleten **Get-AzureRmLogProfile** hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="99dbf-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="99dbf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99dbf-107">EXAMPLES</span></span>

## <span data-ttu-id="99dbf-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99dbf-108">PARAMETERS</span></span>

### <span data-ttu-id="99dbf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99dbf-109">-DefaultProfile</span></span>
<span data-ttu-id="99dbf-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="99dbf-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99dbf-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="99dbf-111">-Name</span></span>
<span data-ttu-id="99dbf-112">Anger namnet på den logg profil som ska visas.</span><span class="sxs-lookup"><span data-stu-id="99dbf-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99dbf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99dbf-113">CommonParameters</span></span>
<span data-ttu-id="99dbf-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99dbf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99dbf-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99dbf-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99dbf-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99dbf-116">INPUTS</span></span>

### <span data-ttu-id="99dbf-117">System. String</span><span class="sxs-lookup"><span data-stu-id="99dbf-117">System.String</span></span>

## <span data-ttu-id="99dbf-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99dbf-118">OUTPUTS</span></span>

### <span data-ttu-id="99dbf-119">Microsoft. Azure. commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="99dbf-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="99dbf-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99dbf-120">NOTES</span></span>

## <span data-ttu-id="99dbf-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99dbf-121">RELATED LINKS</span></span>

[<span data-ttu-id="99dbf-122">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="99dbf-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="99dbf-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="99dbf-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


