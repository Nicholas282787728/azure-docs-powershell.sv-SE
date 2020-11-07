---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 5db21871b84801d57deebf98e27bbe153285631a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931521"
---
# <span data-ttu-id="eb51e-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="eb51e-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="eb51e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb51e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb51e-103">Hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="eb51e-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb51e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb51e-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb51e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb51e-105">DESCRIPTION</span></span>
<span data-ttu-id="eb51e-106">Cmdleten **Get-AzureRmContainerService** hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="eb51e-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="eb51e-107">Du kan visa egenskaperna för en behållar tjänst, vilket inkluderar tillstånd, antalet huvud och agenter samt det fullt kvalificerade domän namnet för huvud gruppen och agenten.</span><span class="sxs-lookup"><span data-stu-id="eb51e-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="eb51e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb51e-108">EXAMPLES</span></span>

### <span data-ttu-id="eb51e-109">Exempel 1: skaffa en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="eb51e-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="eb51e-110">Det här kommandot får en behållar tjänst som heter CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="eb51e-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="eb51e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb51e-111">PARAMETERS</span></span>

### <span data-ttu-id="eb51e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb51e-112">-DefaultProfile</span></span>
<span data-ttu-id="eb51e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb51e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb51e-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb51e-114">-Name</span></span>
<span data-ttu-id="eb51e-115">Anger namnet på den behållar tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="eb51e-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb51e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb51e-116">-ResourceGroupName</span></span>
<span data-ttu-id="eb51e-117">Anger resurs gruppen för den behållar tjänst som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="eb51e-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb51e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb51e-118">CommonParameters</span></span>
<span data-ttu-id="eb51e-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb51e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb51e-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb51e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb51e-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb51e-121">INPUTS</span></span>

### <span data-ttu-id="eb51e-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="eb51e-122">None</span></span>
<span data-ttu-id="eb51e-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="eb51e-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb51e-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb51e-124">OUTPUTS</span></span>

### <span data-ttu-id="eb51e-125">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="eb51e-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="eb51e-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb51e-126">NOTES</span></span>

## <span data-ttu-id="eb51e-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb51e-127">RELATED LINKS</span></span>

[<span data-ttu-id="eb51e-128">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="eb51e-128">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="eb51e-129">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="eb51e-129">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="eb51e-130">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="eb51e-130">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


