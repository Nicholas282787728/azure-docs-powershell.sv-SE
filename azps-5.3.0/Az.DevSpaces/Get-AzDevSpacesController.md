---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426315"
---
# <span data-ttu-id="a58e1-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="a58e1-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="a58e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a58e1-102">SYNOPSIS</span></span>
<span data-ttu-id="a58e1-103">Skaffa eller lista Azure DevSpaces-styrenheten.</span><span class="sxs-lookup"><span data-stu-id="a58e1-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="a58e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a58e1-104">SYNTAX</span></span>

### <span data-ttu-id="a58e1-105">ListDevSpacesControllerParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a58e1-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a58e1-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a58e1-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a58e1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a58e1-107">DESCRIPTION</span></span>
<span data-ttu-id="a58e1-108">Skaffa eller lista Azure DevSpaces-styrenheten.</span><span class="sxs-lookup"><span data-stu-id="a58e1-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="a58e1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a58e1-109">EXAMPLES</span></span>

### <span data-ttu-id="a58e1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a58e1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="a58e1-111">Visa alla styrenheter i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a58e1-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="a58e1-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a58e1-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="a58e1-113">Skaffa en DevSpaces-styrenhet i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a58e1-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="a58e1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a58e1-114">PARAMETERS</span></span>

### <span data-ttu-id="a58e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58e1-115">-DefaultProfile</span></span>
<span data-ttu-id="a58e1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a58e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a58e1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a58e1-117">-Name</span></span>
<span data-ttu-id="a58e1-118">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="a58e1-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a58e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="a58e1-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a58e1-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58e1-121">CommonParameters</span></span>
<span data-ttu-id="a58e1-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a58e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58e1-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a58e1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58e1-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a58e1-124">INPUTS</span></span>

### <span data-ttu-id="a58e1-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="a58e1-125">None</span></span>

## <span data-ttu-id="a58e1-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a58e1-126">OUTPUTS</span></span>

### <span data-ttu-id="a58e1-127">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="a58e1-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="a58e1-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a58e1-128">NOTES</span></span>

## <span data-ttu-id="a58e1-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a58e1-129">RELATED LINKS</span></span>
