---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservicelocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServiceLocation.md
ms.openlocfilehash: 6f869cee7258c38e941ca8fbb7c8ac31b47171af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408328"
---
# <span data-ttu-id="58e8e-101">Get-AzPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="58e8e-101">Get-AzPeeringServiceLocation</span></span>

## <span data-ttu-id="58e8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="58e8e-103">Hämtar en lista över peering service-platser som tillhandahålls av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="58e8e-103">Gets a list of peering service locations offered by Microsoft.</span></span>

## <span data-ttu-id="58e8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58e8e-104">SYNTAX</span></span>

```
Get-AzPeeringServiceLocation [-Country <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58e8e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58e8e-105">DESCRIPTION</span></span>
<span data-ttu-id="58e8e-106">Lista över peer-webbplatser.</span><span class="sxs-lookup"><span data-stu-id="58e8e-106">List peering locations.</span></span>

## <span data-ttu-id="58e8e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58e8e-107">EXAMPLES</span></span>

### <span data-ttu-id="58e8e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="58e8e-108">Example 1</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States" | Where-Object { $_.State -match "Washington"}

Country     : United States
State       : Washington
AzureRegion : West US
Name        : Washington
Id          :
Type        : Microsoft.Peering/peeringServiceLocations
```

<span data-ttu-id="58e8e-109">Hämtar peering-platserna för Washington.</span><span class="sxs-lookup"><span data-stu-id="58e8e-109">Retrieves the peering locations for washington.</span></span>

### <span data-ttu-id="58e8e-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="58e8e-110">Example 2</span></span>
```powershell
PS C:\>Get-AzPeeringServiceLocation -Country "United States"

Country     : United States
State       : Alabama
AzureRegion : East US
Name        : Alabama
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

Country     : United States
State       : Arizona
AzureRegion : West US
Name        : Arizona
Id          :
Type        : Microsoft.Peering/peeringServiceLocations

...
```

<span data-ttu-id="58e8e-111">Hämtar peering-platserna för Washington.</span><span class="sxs-lookup"><span data-stu-id="58e8e-111">Retrieves the peering locations for washington.</span></span>

## <span data-ttu-id="58e8e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58e8e-112">PARAMETERS</span></span>

### <span data-ttu-id="58e8e-113">-Country</span><span class="sxs-lookup"><span data-stu-id="58e8e-113">-Country</span></span>
<span data-ttu-id="58e8e-114">Filtret land</span><span class="sxs-lookup"><span data-stu-id="58e8e-114">The country filter</span></span>

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

### <span data-ttu-id="58e8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e8e-115">-DefaultProfile</span></span>
<span data-ttu-id="58e8e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58e8e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e8e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e8e-117">CommonParameters</span></span>
<span data-ttu-id="58e8e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e8e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e8e-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58e8e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e8e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58e8e-120">INPUTS</span></span>

### <span data-ttu-id="58e8e-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="58e8e-121">None</span></span>

## <span data-ttu-id="58e8e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58e8e-122">OUTPUTS</span></span>

### <span data-ttu-id="58e8e-123">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringServiceLocation</span><span class="sxs-lookup"><span data-stu-id="58e8e-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServiceLocation</span></span>

## <span data-ttu-id="58e8e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58e8e-124">NOTES</span></span>

## <span data-ttu-id="58e8e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58e8e-125">RELATED LINKS</span></span>
