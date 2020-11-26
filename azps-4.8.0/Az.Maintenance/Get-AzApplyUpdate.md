---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259383"
---
# <span data-ttu-id="c7f88-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="c7f88-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="c7f88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7f88-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f88-103">Spåra underhålls uppdateringar för resursen</span><span class="sxs-lookup"><span data-stu-id="c7f88-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="c7f88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7f88-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f88-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7f88-105">DESCRIPTION</span></span>
<span data-ttu-id="c7f88-106">Spåra underhålls uppdateringar för resursen</span><span class="sxs-lookup"><span data-stu-id="c7f88-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="c7f88-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7f88-107">EXAMPLES</span></span>

### <span data-ttu-id="c7f88-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c7f88-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="c7f88-109">Spåra underhålls uppdateringar för resursen</span><span class="sxs-lookup"><span data-stu-id="c7f88-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="c7f88-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7f88-110">PARAMETERS</span></span>

### <span data-ttu-id="c7f88-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="c7f88-111">-ApplyUpdateName</span></span>
<span data-ttu-id="c7f88-112">Resurs namn för Använd uppdatering.</span><span class="sxs-lookup"><span data-stu-id="c7f88-112">The apply update resource name.</span></span>

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

### <span data-ttu-id="c7f88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f88-113">-DefaultProfile</span></span>
<span data-ttu-id="c7f88-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7f88-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7f88-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="c7f88-115">-ProviderName</span></span>
<span data-ttu-id="c7f88-116">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="c7f88-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="c7f88-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f88-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7f88-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c7f88-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="c7f88-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c7f88-119">-ResourceName</span></span>
<span data-ttu-id="c7f88-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="c7f88-120">The resource name.</span></span>

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

### <span data-ttu-id="c7f88-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="c7f88-121">-ResourceParentName</span></span>
<span data-ttu-id="c7f88-122">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="c7f88-122">The parent resource name.</span></span>

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

### <span data-ttu-id="c7f88-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="c7f88-123">-ResourceParentType</span></span>
<span data-ttu-id="c7f88-124">Den överordnade resurs typen.</span><span class="sxs-lookup"><span data-stu-id="c7f88-124">The parent resource type.</span></span>

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

### <span data-ttu-id="c7f88-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c7f88-125">-ResourceType</span></span>
<span data-ttu-id="c7f88-126">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="c7f88-126">The resource type.</span></span>

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

### <span data-ttu-id="c7f88-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f88-127">CommonParameters</span></span>
<span data-ttu-id="c7f88-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7f88-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f88-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7f88-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f88-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7f88-130">INPUTS</span></span>

### <span data-ttu-id="c7f88-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c7f88-131">System.String</span></span>

## <span data-ttu-id="c7f88-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7f88-132">OUTPUTS</span></span>

### <span data-ttu-id="c7f88-133">Microsoft. Azure. commands. Maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="c7f88-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="c7f88-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7f88-134">NOTES</span></span>

## <span data-ttu-id="c7f88-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7f88-135">RELATED LINKS</span></span>