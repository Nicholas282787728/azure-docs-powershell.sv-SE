---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270587"
---
# <span data-ttu-id="b3a59-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="b3a59-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="b3a59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3a59-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a59-103">Visa configurationAssignments för resursen.</span><span class="sxs-lookup"><span data-stu-id="b3a59-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="b3a59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3a59-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3a59-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3a59-105">DESCRIPTION</span></span>
<span data-ttu-id="b3a59-106">Visa configurationAssignments för resursen.</span><span class="sxs-lookup"><span data-stu-id="b3a59-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="b3a59-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3a59-107">EXAMPLES</span></span>

### <span data-ttu-id="b3a59-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b3a59-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="b3a59-109">Lista configurationAssignments för dedikerad värd.</span><span class="sxs-lookup"><span data-stu-id="b3a59-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="b3a59-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3a59-110">PARAMETERS</span></span>

### <span data-ttu-id="b3a59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a59-111">-DefaultProfile</span></span>
<span data-ttu-id="b3a59-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a59-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a59-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="b3a59-113">-ProviderName</span></span>
<span data-ttu-id="b3a59-114">Namnet på resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="b3a59-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="b3a59-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a59-115">-ResourceGroupName</span></span>
<span data-ttu-id="b3a59-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b3a59-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="b3a59-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b3a59-117">-ResourceName</span></span>
<span data-ttu-id="b3a59-118">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="b3a59-118">The resource name.</span></span>

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

### <span data-ttu-id="b3a59-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="b3a59-119">-ResourceParentName</span></span>
<span data-ttu-id="b3a59-120">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="b3a59-120">The parent resource name.</span></span>

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

### <span data-ttu-id="b3a59-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="b3a59-121">-ResourceParentType</span></span>
<span data-ttu-id="b3a59-122">Den överordnade resurs typen.</span><span class="sxs-lookup"><span data-stu-id="b3a59-122">The parent resource type.</span></span>

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

### <span data-ttu-id="b3a59-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b3a59-123">-ResourceType</span></span>
<span data-ttu-id="b3a59-124">Resurs typen.</span><span class="sxs-lookup"><span data-stu-id="b3a59-124">The resource type.</span></span>

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

### <span data-ttu-id="b3a59-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a59-125">CommonParameters</span></span>
<span data-ttu-id="b3a59-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a59-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a59-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3a59-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a59-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3a59-128">INPUTS</span></span>

### <span data-ttu-id="b3a59-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b3a59-129">System.String</span></span>

## <span data-ttu-id="b3a59-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3a59-130">OUTPUTS</span></span>

### <span data-ttu-id="b3a59-131">Microsoft. Azure. commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="b3a59-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="b3a59-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3a59-132">NOTES</span></span>

## <span data-ttu-id="b3a59-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3a59-133">RELATED LINKS</span></span>
