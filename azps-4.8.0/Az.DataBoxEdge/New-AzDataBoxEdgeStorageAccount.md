---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 2a5a1314f422a7b91a5cc8885abe0af98fa395a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260275"
---
# <span data-ttu-id="6cc64-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6cc64-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="6cc64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cc64-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc64-103">Skapar ett nytt Edge Storage-konto i enheten.</span><span class="sxs-lookup"><span data-stu-id="6cc64-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="6cc64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cc64-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cc64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cc64-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc64-106">Cmdleten **New-AzDataBoxEdgeStorageAccount** skapar ett nytt gräns lagrings konto i en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="6cc64-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="6cc64-107">För en enhet går det bara att mappa ett gräns lagrings konto högst till ett moln lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6cc64-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="6cc64-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cc64-108">EXAMPLES</span></span>

### <span data-ttu-id="6cc64-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6cc64-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="6cc64-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6cc64-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="6cc64-111">2 EdgeStorageAccounts på enheten kan inte dela mer än 1 moln lagrings konto</span><span class="sxs-lookup"><span data-stu-id="6cc64-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="6cc64-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cc64-112">PARAMETERS</span></span>

### <span data-ttu-id="6cc64-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cc64-113">-AsJob</span></span>
<span data-ttu-id="6cc64-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6cc64-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cc64-115">-Molnet</span><span class="sxs-lookup"><span data-stu-id="6cc64-115">-Cloud</span></span>
<span data-ttu-id="6cc64-116">Använder en CloudStorageAccount för skiktning</span><span class="sxs-lookup"><span data-stu-id="6cc64-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc64-117">-DefaultProfile</span></span>
<span data-ttu-id="6cc64-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cc64-119">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="6cc64-119">-DeviceName</span></span>
<span data-ttu-id="6cc64-120">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="6cc64-120">Device Name</span></span>

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

### <span data-ttu-id="6cc64-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="6cc64-121">-Name</span></span>
<span data-ttu-id="6cc64-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="6cc64-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc64-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc64-123">-ResourceGroupName</span></span>
<span data-ttu-id="6cc64-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6cc64-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6cc64-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="6cc64-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="6cc64-126">Ange befintligt StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6cc64-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc64-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6cc64-127">-Confirm</span></span>
<span data-ttu-id="6cc64-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6cc64-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc64-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc64-129">-WhatIf</span></span>
<span data-ttu-id="6cc64-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6cc64-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cc64-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6cc64-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc64-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc64-132">CommonParameters</span></span>
<span data-ttu-id="6cc64-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc64-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc64-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cc64-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc64-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cc64-135">INPUTS</span></span>

### <span data-ttu-id="6cc64-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6cc64-136">System.String</span></span>

### <span data-ttu-id="6cc64-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6cc64-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6cc64-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cc64-138">OUTPUTS</span></span>

### <span data-ttu-id="6cc64-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6cc64-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="6cc64-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cc64-140">NOTES</span></span>

## <span data-ttu-id="6cc64-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cc64-141">RELATED LINKS</span></span>