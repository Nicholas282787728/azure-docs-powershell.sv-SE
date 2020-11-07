---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: a3f650861f70ad9110f4716e5034cd5e7f930343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757391"
---
# <span data-ttu-id="430fe-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="430fe-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="430fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="430fe-102">SYNOPSIS</span></span>
<span data-ttu-id="430fe-103">Tar bort en data källa.</span><span class="sxs-lookup"><span data-stu-id="430fe-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="430fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="430fe-104">SYNTAX</span></span>

### <span data-ttu-id="430fe-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="430fe-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="430fe-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="430fe-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="430fe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="430fe-107">DESCRIPTION</span></span>
<span data-ttu-id="430fe-108">Cmdleten **Remove-AzureRmOperationalInsightsDataSource** tar bort en data källa.</span><span class="sxs-lookup"><span data-stu-id="430fe-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="430fe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="430fe-109">EXAMPLES</span></span>

## <span data-ttu-id="430fe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="430fe-110">PARAMETERS</span></span>

### <span data-ttu-id="430fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="430fe-111">-DefaultProfile</span></span>
<span data-ttu-id="430fe-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="430fe-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="430fe-113">-Force</span><span class="sxs-lookup"><span data-stu-id="430fe-113">-Force</span></span>
<span data-ttu-id="430fe-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="430fe-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fe-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="430fe-115">-Name</span></span>
<span data-ttu-id="430fe-116">Anger namnet på den data källa som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="430fe-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="430fe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="430fe-117">-ResourceGroupName</span></span>
<span data-ttu-id="430fe-118">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="430fe-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="430fe-119">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="430fe-119">-Workspace</span></span>
<span data-ttu-id="430fe-120">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="430fe-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="430fe-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="430fe-121">-WorkspaceName</span></span>
<span data-ttu-id="430fe-122">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="430fe-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="430fe-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="430fe-123">-Confirm</span></span>
<span data-ttu-id="430fe-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="430fe-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="430fe-125">-WhatIf</span></span>
<span data-ttu-id="430fe-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="430fe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="430fe-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="430fe-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="430fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="430fe-128">CommonParameters</span></span>
<span data-ttu-id="430fe-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="430fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="430fe-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="430fe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="430fe-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="430fe-131">INPUTS</span></span>

### <span data-ttu-id="430fe-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="430fe-132">PSWorkspace</span></span>
<span data-ttu-id="430fe-133">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="430fe-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="430fe-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="430fe-134">OUTPUTS</span></span>

## <span data-ttu-id="430fe-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="430fe-135">NOTES</span></span>
* <span data-ttu-id="430fe-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="430fe-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="430fe-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="430fe-137">RELATED LINKS</span></span>

[<span data-ttu-id="430fe-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="430fe-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="430fe-139">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="430fe-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


