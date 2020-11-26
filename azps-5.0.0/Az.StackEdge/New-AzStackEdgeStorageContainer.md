---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269744"
---
# <span data-ttu-id="37ab7-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="37ab7-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="37ab7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="37ab7-103">Skapar en ny lagrings behållare i Edge Storage-kontot på enheten.</span><span class="sxs-lookup"><span data-stu-id="37ab7-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="37ab7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37ab7-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37ab7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="37ab7-106">Cmdleten **New-AzStackEdgeStorageContainer** skapar en ny lagrings behållare i Edge Storage-kontot på en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="37ab7-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="37ab7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37ab7-107">EXAMPLES</span></span>

### <span data-ttu-id="37ab7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="37ab7-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="37ab7-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37ab7-109">PARAMETERS</span></span>

### <span data-ttu-id="37ab7-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37ab7-110">-AsJob</span></span>
<span data-ttu-id="37ab7-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="37ab7-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="37ab7-112">-DataFormat</span></span>
<span data-ttu-id="37ab7-113">Ange data format från t ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="37ab7-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="37ab7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ab7-114">-DefaultProfile</span></span>
<span data-ttu-id="37ab7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37ab7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37ab7-116">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="37ab7-116">-DeviceName</span></span>
<span data-ttu-id="37ab7-117">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="37ab7-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="37ab7-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="37ab7-119">Ange befintliga EdgeStorageAccount namn</span><span class="sxs-lookup"><span data-stu-id="37ab7-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="37ab7-120">-Name</span></span>
<span data-ttu-id="37ab7-121">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="37ab7-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ab7-122">-ResourceGroupName</span></span>
<span data-ttu-id="37ab7-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="37ab7-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37ab7-124">-Confirm</span></span>
<span data-ttu-id="37ab7-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37ab7-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ab7-126">-WhatIf</span></span>
<span data-ttu-id="37ab7-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37ab7-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37ab7-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37ab7-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ab7-129">CommonParameters</span></span>
<span data-ttu-id="37ab7-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ab7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ab7-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37ab7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ab7-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37ab7-132">INPUTS</span></span>

### <span data-ttu-id="37ab7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="37ab7-133">System.String</span></span>

## <span data-ttu-id="37ab7-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37ab7-134">OUTPUTS</span></span>

### <span data-ttu-id="37ab7-135">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="37ab7-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="37ab7-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37ab7-136">NOTES</span></span>

## <span data-ttu-id="37ab7-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37ab7-137">RELATED LINKS</span></span>