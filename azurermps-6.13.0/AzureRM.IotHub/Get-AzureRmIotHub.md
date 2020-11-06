---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 44cb5e9317c1806200a571dd6311e212e50a8c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576262"
---
# <span data-ttu-id="672e3-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="672e3-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="672e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="672e3-102">SYNOPSIS</span></span>
<span data-ttu-id="672e3-103">Hämtar information om IotHubs i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="672e3-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="672e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="672e3-104">SYNTAX</span></span>

### <span data-ttu-id="672e3-105">ListIotHubsByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="672e3-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="672e3-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="672e3-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="672e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="672e3-107">DESCRIPTION</span></span>
<span data-ttu-id="672e3-108">Hämtar information om IotHubs i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="672e3-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="672e3-109">Du kan visa alla IotHub-instanser i ett abonnemang eller filtrera dina resultat efter en resurs grupp eller ett visst IotHub-namn.</span><span class="sxs-lookup"><span data-stu-id="672e3-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="672e3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="672e3-110">EXAMPLES</span></span>

### <span data-ttu-id="672e3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="672e3-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="672e3-112">Hämtar alla IotHubs i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="672e3-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="672e3-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="672e3-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="672e3-114">Hämtar alla IotHubs i prenumerationen som tillhör resourcegroup med namnet "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="672e3-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="672e3-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="672e3-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="672e3-116">Hämtar information om IotHub med namnet "myiothub".</span><span class="sxs-lookup"><span data-stu-id="672e3-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="672e3-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="672e3-117">PARAMETERS</span></span>

### <span data-ttu-id="672e3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672e3-118">-DefaultProfile</span></span>
<span data-ttu-id="672e3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="672e3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="672e3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="672e3-120">-Name</span></span>
<span data-ttu-id="672e3-121">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="672e3-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="672e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="672e3-123">Namn på ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="672e3-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="672e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672e3-124">CommonParameters</span></span>
<span data-ttu-id="672e3-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="672e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672e3-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="672e3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672e3-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="672e3-127">INPUTS</span></span>

### <span data-ttu-id="672e3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="672e3-128">System.String</span></span>

## <span data-ttu-id="672e3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="672e3-129">OUTPUTS</span></span>

### <span data-ttu-id="672e3-130">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="672e3-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="672e3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="672e3-131">NOTES</span></span>

## <span data-ttu-id="672e3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="672e3-132">RELATED LINKS</span></span>
