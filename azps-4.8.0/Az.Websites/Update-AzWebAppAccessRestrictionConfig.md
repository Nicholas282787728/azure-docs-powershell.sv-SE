---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100667"
---
# <span data-ttu-id="60403-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="60403-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="60403-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60403-102">SYNOPSIS</span></span>
<span data-ttu-id="60403-103">Uppdaterar arv av huvud webbplats åtkomst Restiction config till SCM-webbplatsen för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="60403-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="60403-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60403-104">SYNTAX</span></span>

### <span data-ttu-id="60403-105">InputValuesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="60403-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60403-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60403-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60403-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60403-107">DESCRIPTION</span></span>
<span data-ttu-id="60403-108">Cmdleten **Update-AzWebAppAccessRestrictionConfig** uppdaterar åtkomst begränsnings konfiguration för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="60403-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="60403-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60403-109">EXAMPLES</span></span>

### <span data-ttu-id="60403-110">Exempel 1: uppdatera en Web App-webbplats för att använda åtkomst begränsningar från huvud webbplatsen</span><span class="sxs-lookup"><span data-stu-id="60403-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="60403-111">Följande exempel uppdaterar ett webb program som heter IpRule som tillhör resurs gruppen MyResourceGroup för att använda åtkomst begränsnings konfiguration för huvud webbplatsen på SCM-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="60403-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="60403-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60403-112">PARAMETERS</span></span>

### <span data-ttu-id="60403-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60403-113">-DefaultProfile</span></span>
<span data-ttu-id="60403-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60403-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60403-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60403-115">-InputObject</span></span>
<span data-ttu-id="60403-116">Konfigurations objekt för begränsning av åtkomst</span><span class="sxs-lookup"><span data-stu-id="60403-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60403-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="60403-117">-Name</span></span>
<span data-ttu-id="60403-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="60403-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60403-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60403-119">-PassThru</span></span>
<span data-ttu-id="60403-120">Returnera konfigurations objekt för åtkomst begränsning.</span><span class="sxs-lookup"><span data-stu-id="60403-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="60403-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60403-121">-ResourceGroupName</span></span>
<span data-ttu-id="60403-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="60403-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60403-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="60403-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="60403-124">SCM-webbplatsen ärver regler som är inställda på huvud webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="60403-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="60403-125">-SlotName</span></span>
<span data-ttu-id="60403-126">Namn på distributions platsen.</span><span class="sxs-lookup"><span data-stu-id="60403-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60403-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="60403-127">-Confirm</span></span>
<span data-ttu-id="60403-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="60403-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60403-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60403-129">-WhatIf</span></span>
<span data-ttu-id="60403-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="60403-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60403-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="60403-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60403-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60403-132">CommonParameters</span></span>
<span data-ttu-id="60403-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60403-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60403-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60403-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60403-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60403-135">INPUTS</span></span>

### <span data-ttu-id="60403-136">System. String</span><span class="sxs-lookup"><span data-stu-id="60403-136">System.String</span></span>

### <span data-ttu-id="60403-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="60403-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60403-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60403-138">OUTPUTS</span></span>

### <span data-ttu-id="60403-139">Microsoft. Azure. commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="60403-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="60403-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60403-140">NOTES</span></span>

## <span data-ttu-id="60403-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60403-141">RELATED LINKS</span></span>

[<span data-ttu-id="60403-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="60403-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="60403-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="60403-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="60403-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="60403-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)