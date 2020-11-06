---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 49674f372e477ee7050a6ccf7d833aaee59bac3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575914"
---
# <span data-ttu-id="f239b-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f239b-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="f239b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f239b-102">SYNOPSIS</span></span>
<span data-ttu-id="f239b-103">Tar bort en data källa.</span><span class="sxs-lookup"><span data-stu-id="f239b-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f239b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f239b-104">SYNTAX</span></span>

### <span data-ttu-id="f239b-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="f239b-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f239b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f239b-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f239b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f239b-107">DESCRIPTION</span></span>
<span data-ttu-id="f239b-108">Cmdleten **Remove-AzureRmOperationalInsightsDataSource** tar bort en data källa.</span><span class="sxs-lookup"><span data-stu-id="f239b-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="f239b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f239b-109">EXAMPLES</span></span>

## <span data-ttu-id="f239b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f239b-110">PARAMETERS</span></span>

### <span data-ttu-id="f239b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f239b-111">-Force</span></span>
<span data-ttu-id="f239b-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f239b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f239b-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="f239b-113">-Name</span></span>
<span data-ttu-id="f239b-114">Anger namnet på den data källa som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f239b-114">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="f239b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f239b-115">-ResourceGroupName</span></span>
<span data-ttu-id="f239b-116">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="f239b-116">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f239b-117">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="f239b-117">-Workspace</span></span>
<span data-ttu-id="f239b-118">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="f239b-118">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f239b-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f239b-119">-WorkspaceName</span></span>
<span data-ttu-id="f239b-120">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="f239b-120">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f239b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f239b-121">-Confirm</span></span>
<span data-ttu-id="f239b-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f239b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f239b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f239b-123">-WhatIf</span></span>
<span data-ttu-id="f239b-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f239b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f239b-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f239b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f239b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f239b-126">-DefaultProfile</span></span>
<span data-ttu-id="f239b-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f239b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f239b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f239b-128">CommonParameters</span></span>
<span data-ttu-id="f239b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f239b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f239b-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f239b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f239b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f239b-131">INPUTS</span></span>

### <span data-ttu-id="f239b-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f239b-132">PSWorkspace</span></span>
<span data-ttu-id="f239b-133">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f239b-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="f239b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f239b-134">OUTPUTS</span></span>

## <span data-ttu-id="f239b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f239b-135">NOTES</span></span>
* <span data-ttu-id="f239b-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="f239b-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f239b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f239b-137">RELATED LINKS</span></span>

[<span data-ttu-id="f239b-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f239b-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="f239b-139">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f239b-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


