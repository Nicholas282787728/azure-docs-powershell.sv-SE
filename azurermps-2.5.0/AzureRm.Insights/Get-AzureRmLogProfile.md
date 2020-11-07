---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 29ff6159501bccd73947e25a65ec765a49b8859c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928881"
---
# <span data-ttu-id="d7bfb-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="d7bfb-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="d7bfb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bfb-103">Hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7bfb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7bfb-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7bfb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="d7bfb-106">Cmdleten **Get-AzureRmLogProfile** hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="d7bfb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7bfb-107">EXAMPLES</span></span>

## <span data-ttu-id="d7bfb-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7bfb-108">PARAMETERS</span></span>

### <span data-ttu-id="d7bfb-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bfb-109">-DefaultProfile</span></span>
<span data-ttu-id="d7bfb-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d7bfb-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7bfb-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7bfb-111">-Name</span></span>
<span data-ttu-id="d7bfb-112">Anger namnet på den logg profil som ska visas.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="d7bfb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bfb-113">CommonParameters</span></span>
<span data-ttu-id="d7bfb-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7bfb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bfb-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bfb-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bfb-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7bfb-116">INPUTS</span></span>

### <span data-ttu-id="d7bfb-117">System. String</span><span class="sxs-lookup"><span data-stu-id="d7bfb-117">System.String</span></span>

## <span data-ttu-id="d7bfb-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7bfb-118">OUTPUTS</span></span>

### <span data-ttu-id="d7bfb-119">Microsoft. Azure. commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="d7bfb-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="d7bfb-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7bfb-120">NOTES</span></span>

## <span data-ttu-id="d7bfb-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7bfb-121">RELATED LINKS</span></span>

[<span data-ttu-id="d7bfb-122">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="d7bfb-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="d7bfb-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="d7bfb-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


