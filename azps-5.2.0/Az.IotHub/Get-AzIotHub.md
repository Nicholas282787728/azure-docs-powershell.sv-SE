---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402283"
---
# <span data-ttu-id="f48bc-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="f48bc-101">Get-AzIotHub</span></span>

## <span data-ttu-id="f48bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f48bc-102">SYNOPSIS</span></span>
<span data-ttu-id="f48bc-103">Hämtar information om IotHubs i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f48bc-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="f48bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f48bc-104">SYNTAX</span></span>

### <span data-ttu-id="f48bc-105">ListIotHubsByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="f48bc-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f48bc-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="f48bc-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f48bc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f48bc-107">DESCRIPTION</span></span>
<span data-ttu-id="f48bc-108">Hämtar information om IotHubs i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f48bc-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="f48bc-109">Du kan visa alla IotHub-instanser i ett abonnemang eller filtrera dina resultat efter en resurs grupp eller ett visst IotHub-namn.</span><span class="sxs-lookup"><span data-stu-id="f48bc-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="f48bc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f48bc-110">EXAMPLES</span></span>

### <span data-ttu-id="f48bc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f48bc-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="f48bc-112">Hämtar alla IotHubs i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f48bc-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="f48bc-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f48bc-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="f48bc-114">Hämtar alla IotHubs i prenumerationen som tillhör resourcegroup med namnet "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="f48bc-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="f48bc-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="f48bc-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f48bc-116">Hämtar information om IotHub med namnet "myiothub".</span><span class="sxs-lookup"><span data-stu-id="f48bc-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="f48bc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f48bc-117">PARAMETERS</span></span>

### <span data-ttu-id="f48bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48bc-118">-DefaultProfile</span></span>
<span data-ttu-id="f48bc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f48bc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f48bc-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f48bc-120">-Name</span></span>
<span data-ttu-id="f48bc-121">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="f48bc-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f48bc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f48bc-122">-ResourceGroupName</span></span>
<span data-ttu-id="f48bc-123">Namn på ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f48bc-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f48bc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48bc-124">CommonParameters</span></span>
<span data-ttu-id="f48bc-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48bc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48bc-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f48bc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48bc-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f48bc-127">INPUTS</span></span>

### <span data-ttu-id="f48bc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f48bc-128">System.String</span></span>

## <span data-ttu-id="f48bc-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f48bc-129">OUTPUTS</span></span>

### <span data-ttu-id="f48bc-130">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f48bc-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="f48bc-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f48bc-131">NOTES</span></span>

## <span data-ttu-id="f48bc-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f48bc-132">RELATED LINKS</span></span>
