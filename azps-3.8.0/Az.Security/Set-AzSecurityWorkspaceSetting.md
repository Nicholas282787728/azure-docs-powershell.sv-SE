---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 2e74751b3f64c3192e7983188ae66cde021f0e3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091490"
---
# <span data-ttu-id="9d2ba-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9d2ba-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9d2ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d2ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9d2ba-103">Uppdaterar arbets ytans inställningar för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="9d2ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d2ba-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d2ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d2ba-105">DESCRIPTION</span></span>
<span data-ttu-id="9d2ba-106">Uppdaterar arbets ytans inställningar för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="9d2ba-107">Den konfigurerade arbets ytan innehåller säkerhets data som samlats in av agenten för Azure logganalys Analytics som är installerad på virtuella datorer i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="9d2ba-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d2ba-108">EXAMPLES</span></span>

### <span data-ttu-id="9d2ba-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9d2ba-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="9d2ba-110">Anger arbets ytan "yta" för att lagra alla säkerhets data som samlats in av Azure logganalys Analytics-agenten.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="9d2ba-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d2ba-111">PARAMETERS</span></span>

### <span data-ttu-id="9d2ba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d2ba-112">-DefaultProfile</span></span>
<span data-ttu-id="9d2ba-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d2ba-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d2ba-114">-Name</span></span>
<span data-ttu-id="9d2ba-115">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-115">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d2ba-116">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="9d2ba-116">-Scope</span></span>
<span data-ttu-id="9d2ba-117">Sitt.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-117">Scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d2ba-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="9d2ba-118">-WorkspaceId</span></span>
<span data-ttu-id="9d2ba-119">Arbetsyte-ID.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-119">Workspace ID.</span></span>

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

### <span data-ttu-id="9d2ba-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9d2ba-120">-Confirm</span></span>
<span data-ttu-id="9d2ba-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d2ba-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d2ba-122">-WhatIf</span></span>
<span data-ttu-id="9d2ba-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d2ba-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d2ba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d2ba-125">CommonParameters</span></span>
<span data-ttu-id="9d2ba-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d2ba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d2ba-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d2ba-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d2ba-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d2ba-128">INPUTS</span></span>

### <span data-ttu-id="9d2ba-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9d2ba-129">System.String</span></span>

## <span data-ttu-id="9d2ba-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d2ba-130">OUTPUTS</span></span>

### <span data-ttu-id="9d2ba-131">Microsoft. Azure. commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9d2ba-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9d2ba-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d2ba-132">NOTES</span></span>

## <span data-ttu-id="9d2ba-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d2ba-133">RELATED LINKS</span></span>
