---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270647"
---
# <span data-ttu-id="16c6a-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="16c6a-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="16c6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="16c6a-103">Skapa PSHeaderAction-objekt.</span><span class="sxs-lookup"><span data-stu-id="16c6a-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="16c6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16c6a-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16c6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="16c6a-106">Skapar PSHeaderAction-objekt för att skapa PSRulesEngineAction-objekt.</span><span class="sxs-lookup"><span data-stu-id="16c6a-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="16c6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="16c6a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16c6a-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="16c6a-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16c6a-109">PARAMETERS</span></span>

### <span data-ttu-id="16c6a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c6a-110">-DefaultProfile</span></span>
<span data-ttu-id="16c6a-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16c6a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c6a-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="16c6a-112">-HeaderActionType</span></span>
<span data-ttu-id="16c6a-113">Vilken typ av manipulering som ska gälla för rubriken.</span><span class="sxs-lookup"><span data-stu-id="16c6a-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c6a-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="16c6a-114">-HeaderName</span></span>
<span data-ttu-id="16c6a-115">Namnet på den rubrik som åtgärden ska gälla för.</span><span class="sxs-lookup"><span data-stu-id="16c6a-115">The name of the header this action will apply to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c6a-116">-Värde</span><span class="sxs-lookup"><span data-stu-id="16c6a-116">-Value</span></span>
<span data-ttu-id="16c6a-117">Värdet som du vill uppdatera det angivna huvud namnet med.</span><span class="sxs-lookup"><span data-stu-id="16c6a-117">The value to update the given header name with.</span></span>
<span data-ttu-id="16c6a-118">Det här värdet används inte om actionType är Delete.</span><span class="sxs-lookup"><span data-stu-id="16c6a-118">This value is not used if the actionType is Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16c6a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c6a-119">CommonParameters</span></span>
<span data-ttu-id="16c6a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16c6a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c6a-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16c6a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c6a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16c6a-122">INPUTS</span></span>

### <span data-ttu-id="16c6a-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="16c6a-123">None</span></span>

## <span data-ttu-id="16c6a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16c6a-124">OUTPUTS</span></span>

### <span data-ttu-id="16c6a-125">Microsoft. Azure. commands. FrontDoor. Models. PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="16c6a-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="16c6a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16c6a-126">NOTES</span></span>

## <span data-ttu-id="16c6a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16c6a-127">RELATED LINKS</span></span>
