---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 8ad5026f0e033c6ab5825c9c862b19ad51b40ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915653"
---
# <span data-ttu-id="5bca3-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="5bca3-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="5bca3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bca3-102">SYNOPSIS</span></span>
<span data-ttu-id="5bca3-103">Hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="5bca3-103">Gets a log profile.</span></span>

## <span data-ttu-id="5bca3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bca3-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bca3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bca3-105">DESCRIPTION</span></span>
<span data-ttu-id="5bca3-106">Cmdleten **Get-AzLogProfile** hämtar en logg profil.</span><span class="sxs-lookup"><span data-stu-id="5bca3-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="5bca3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bca3-107">EXAMPLES</span></span>

## <span data-ttu-id="5bca3-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bca3-108">PARAMETERS</span></span>

### <span data-ttu-id="5bca3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bca3-109">-DefaultProfile</span></span>
<span data-ttu-id="5bca3-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5bca3-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bca3-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="5bca3-111">-Name</span></span>
<span data-ttu-id="5bca3-112">Anger namnet på den logg profil som ska visas.</span><span class="sxs-lookup"><span data-stu-id="5bca3-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="5bca3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bca3-113">CommonParameters</span></span>
<span data-ttu-id="5bca3-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bca3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bca3-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bca3-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bca3-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bca3-116">INPUTS</span></span>

### <span data-ttu-id="5bca3-117">System. String</span><span class="sxs-lookup"><span data-stu-id="5bca3-117">System.String</span></span>

## <span data-ttu-id="5bca3-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bca3-118">OUTPUTS</span></span>

### <span data-ttu-id="5bca3-119">Microsoft. Azure. commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="5bca3-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="5bca3-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bca3-120">NOTES</span></span>

## <span data-ttu-id="5bca3-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bca3-121">RELATED LINKS</span></span>

[<span data-ttu-id="5bca3-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="5bca3-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="5bca3-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="5bca3-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)

