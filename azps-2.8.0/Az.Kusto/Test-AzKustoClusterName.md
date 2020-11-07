---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: 9a3d8397914317d733c8da47e7d095e1acb541e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743830"
---
# <span data-ttu-id="3b27b-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="3b27b-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="3b27b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b27b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b27b-103">Kontrol lera om det finns ett angivet kluster namn för Kusto.</span><span class="sxs-lookup"><span data-stu-id="3b27b-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="3b27b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b27b-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b27b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b27b-105">DESCRIPTION</span></span>
<span data-ttu-id="3b27b-106">Kontrol lera om det finns ett angivet kluster namn för Kusto.</span><span class="sxs-lookup"><span data-stu-id="3b27b-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="3b27b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b27b-107">EXAMPLES</span></span>

### <span data-ttu-id="3b27b-108">Exempel 1 – kontrol lera tillgänglighet för ett Kusto kluster namn som används</span><span class="sxs-lookup"><span data-stu-id="3b27b-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="3b27b-109">Kommandot ovan returnerar om ett Kusto-kluster med namnet "mykustocluster" finns i området "Central USA".</span><span class="sxs-lookup"><span data-stu-id="3b27b-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="3b27b-110">Exempel 2 – kontrol lera tillgänglighet för ett Kusto kluster namn som inte används</span><span class="sxs-lookup"><span data-stu-id="3b27b-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="3b27b-111">Kommandot ovan returnerar om ett Kusto-kluster med namnet "mykustocluster" finns i området "Central USA".</span><span class="sxs-lookup"><span data-stu-id="3b27b-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="3b27b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b27b-112">PARAMETERS</span></span>

### <span data-ttu-id="3b27b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b27b-113">-DefaultProfile</span></span>
<span data-ttu-id="3b27b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b27b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b27b-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="3b27b-115">-Location</span></span>
<span data-ttu-id="3b27b-116">Platsen där du vill kontrol lera.</span><span class="sxs-lookup"><span data-stu-id="3b27b-116">The location where to check.</span></span>

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

### <span data-ttu-id="3b27b-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b27b-117">-Name</span></span>
<span data-ttu-id="3b27b-118">Namn på ett specifikt kluster.</span><span class="sxs-lookup"><span data-stu-id="3b27b-118">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="3b27b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b27b-119">CommonParameters</span></span>
<span data-ttu-id="3b27b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b27b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b27b-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b27b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b27b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b27b-122">INPUTS</span></span>

### <span data-ttu-id="3b27b-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="3b27b-123">None</span></span>

## <span data-ttu-id="3b27b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b27b-124">OUTPUTS</span></span>

### <span data-ttu-id="3b27b-125">Microsoft. Azure. commands. Kusto. Models. PSKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="3b27b-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="3b27b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b27b-126">NOTES</span></span>

## <span data-ttu-id="3b27b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b27b-127">RELATED LINKS</span></span>
