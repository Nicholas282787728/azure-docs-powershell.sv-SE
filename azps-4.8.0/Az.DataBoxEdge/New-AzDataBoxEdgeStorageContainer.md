---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260273"
---
# <span data-ttu-id="06468-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="06468-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="06468-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06468-102">SYNOPSIS</span></span>
<span data-ttu-id="06468-103">Skapar en ny lagrings behållare i Edge Storage-kontot på enheten.</span><span class="sxs-lookup"><span data-stu-id="06468-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="06468-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06468-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06468-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06468-105">DESCRIPTION</span></span>
<span data-ttu-id="06468-106">Cmdleten **New-AzDataBoxEdgeStorageContainer** skapar en ny lagrings behållare i Edge Storage-kontot på en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="06468-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="06468-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06468-107">EXAMPLES</span></span>

### <span data-ttu-id="06468-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06468-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="06468-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06468-109">PARAMETERS</span></span>

### <span data-ttu-id="06468-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06468-110">-AsJob</span></span>
<span data-ttu-id="06468-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="06468-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06468-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="06468-112">-DataFormat</span></span>
<span data-ttu-id="06468-113">Ange data format från t ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="06468-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="06468-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06468-114">-DefaultProfile</span></span>
<span data-ttu-id="06468-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06468-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06468-116">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="06468-116">-DeviceName</span></span>
<span data-ttu-id="06468-117">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="06468-117">Device Name</span></span>

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

### <span data-ttu-id="06468-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="06468-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="06468-119">Ange befintliga EdgeStorageAccount namn</span><span class="sxs-lookup"><span data-stu-id="06468-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="06468-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="06468-120">-Name</span></span>
<span data-ttu-id="06468-121">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="06468-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06468-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06468-122">-ResourceGroupName</span></span>
<span data-ttu-id="06468-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="06468-123">Resource Group Name</span></span>

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

### <span data-ttu-id="06468-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06468-124">-Confirm</span></span>
<span data-ttu-id="06468-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06468-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06468-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06468-126">-WhatIf</span></span>
<span data-ttu-id="06468-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06468-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06468-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06468-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06468-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06468-129">CommonParameters</span></span>
<span data-ttu-id="06468-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06468-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06468-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06468-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06468-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06468-132">INPUTS</span></span>

### <span data-ttu-id="06468-133">System. String</span><span class="sxs-lookup"><span data-stu-id="06468-133">System.String</span></span>

## <span data-ttu-id="06468-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06468-134">OUTPUTS</span></span>

### <span data-ttu-id="06468-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="06468-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="06468-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06468-136">NOTES</span></span>

## <span data-ttu-id="06468-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06468-137">RELATED LINKS</span></span>
