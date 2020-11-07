---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925245"
---
# <span data-ttu-id="bb3d0-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="bb3d0-101">Get-AzContainerService</span></span>

## <span data-ttu-id="bb3d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3d0-103">Hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="bb3d0-103">Gets a container service.</span></span>

## <span data-ttu-id="bb3d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb3d0-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb3d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb3d0-105">DESCRIPTION</span></span>
<span data-ttu-id="bb3d0-106">Cmdleten **Get-AzContainerService** hämtar en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="bb3d0-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="bb3d0-107">Du kan visa egenskaperna för en behållar tjänst, vilket inkluderar tillstånd, antalet huvud och agenter samt det fullt kvalificerade domän namnet för huvud gruppen och agenten.</span><span class="sxs-lookup"><span data-stu-id="bb3d0-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="bb3d0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb3d0-108">EXAMPLES</span></span>

### <span data-ttu-id="bb3d0-109">Exempel 1: skaffa en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="bb3d0-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="bb3d0-110">Det här kommandot får en behållar tjänst som heter CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="bb3d0-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="bb3d0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb3d0-111">PARAMETERS</span></span>

### <span data-ttu-id="bb3d0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3d0-112">-DefaultProfile</span></span>
<span data-ttu-id="bb3d0-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3d0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb3d0-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb3d0-114">-Name</span></span>
<span data-ttu-id="bb3d0-115">Anger namnet på den behållar tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="bb3d0-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bb3d0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb3d0-116">-ResourceGroupName</span></span>
<span data-ttu-id="bb3d0-117">Anger resurs gruppen för den behållar tjänst som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="bb3d0-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bb3d0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3d0-118">CommonParameters</span></span>
<span data-ttu-id="bb3d0-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3d0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3d0-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb3d0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3d0-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb3d0-121">INPUTS</span></span>

### <span data-ttu-id="bb3d0-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="bb3d0-122">None</span></span>
<span data-ttu-id="bb3d0-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bb3d0-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb3d0-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb3d0-124">OUTPUTS</span></span>

### <span data-ttu-id="bb3d0-125">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="bb3d0-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="bb3d0-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb3d0-126">NOTES</span></span>

## <span data-ttu-id="bb3d0-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb3d0-127">RELATED LINKS</span></span>

[<span data-ttu-id="bb3d0-128">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="bb3d0-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="bb3d0-129">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="bb3d0-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="bb3d0-130">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="bb3d0-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


