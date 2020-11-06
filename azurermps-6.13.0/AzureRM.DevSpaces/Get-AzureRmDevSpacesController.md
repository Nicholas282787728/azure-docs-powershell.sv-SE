---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/get-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
ms.openlocfilehash: d0140af9d5345e9f3f68c212ae43403fc0f64280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576299"
---
# <span data-ttu-id="a9cad-101">Get-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="a9cad-101">Get-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="a9cad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9cad-102">SYNOPSIS</span></span>
<span data-ttu-id="a9cad-103">Skaffa eller lista Azure DevSpaces-styrenheten.</span><span class="sxs-lookup"><span data-stu-id="a9cad-103">Get or list Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9cad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9cad-104">SYNTAX</span></span>

### <span data-ttu-id="a9cad-105">ListDevSpacesControllerParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a9cad-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzureRmDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9cad-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9cad-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9cad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9cad-107">DESCRIPTION</span></span>
<span data-ttu-id="a9cad-108">Skaffa eller lista Azure DevSpaces-styrenheten.</span><span class="sxs-lookup"><span data-stu-id="a9cad-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="a9cad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9cad-109">EXAMPLES</span></span>

### <span data-ttu-id="a9cad-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9cad-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="a9cad-111">Visa alla styrenheter i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a9cad-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="a9cad-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a9cad-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="a9cad-113">Skaffa en DevSpaces-styrenhet i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a9cad-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="a9cad-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9cad-114">PARAMETERS</span></span>

### <span data-ttu-id="a9cad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9cad-115">-DefaultProfile</span></span>
<span data-ttu-id="a9cad-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9cad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9cad-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9cad-117">-Name</span></span>
<span data-ttu-id="a9cad-118">Namn på DevSpaces-kontroll.</span><span class="sxs-lookup"><span data-stu-id="a9cad-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="a9cad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9cad-119">-ResourceGroupName</span></span>
<span data-ttu-id="a9cad-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a9cad-120">Resource group name</span></span>

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

### <span data-ttu-id="a9cad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9cad-121">CommonParameters</span></span>
<span data-ttu-id="a9cad-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9cad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9cad-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9cad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9cad-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9cad-124">INPUTS</span></span>

### <span data-ttu-id="a9cad-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="a9cad-125">None</span></span>

## <span data-ttu-id="a9cad-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9cad-126">OUTPUTS</span></span>

### <span data-ttu-id="a9cad-127">Microsoft. Azure. commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="a9cad-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="a9cad-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9cad-128">NOTES</span></span>

## <span data-ttu-id="a9cad-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9cad-129">RELATED LINKS</span></span>
