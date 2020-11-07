---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 679b1458b3e749b2ccfca3863f745edd562ffc2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746947"
---
# <span data-ttu-id="a87a8-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="a87a8-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="a87a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a87a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a87a8-103">Uppdaterar arbets ytans inställningar för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a87a8-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="a87a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a87a8-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a87a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a87a8-105">DESCRIPTION</span></span>
<span data-ttu-id="a87a8-106">Uppdaterar arbets ytans inställningar för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a87a8-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="a87a8-107">Den konfigurerade arbets ytan innehåller säkerhets data som samlats in av säkerhets agenten som är installerad på virtuella datorer i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a87a8-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="a87a8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a87a8-108">EXAMPLES</span></span>

### <span data-ttu-id="a87a8-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a87a8-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="a87a8-110">Ställer in alla säkerhets data som samlats in av säkerhets agenterna i arbets ytan "min arbets yta".</span><span class="sxs-lookup"><span data-stu-id="a87a8-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="a87a8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a87a8-111">PARAMETERS</span></span>

### <span data-ttu-id="a87a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a87a8-112">-DefaultProfile</span></span>
<span data-ttu-id="a87a8-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a87a8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a87a8-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="a87a8-114">-Name</span></span>
<span data-ttu-id="a87a8-115">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a87a8-115">Resource name.</span></span>

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

### <span data-ttu-id="a87a8-116">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="a87a8-116">-Scope</span></span>
<span data-ttu-id="a87a8-117">Sitt.</span><span class="sxs-lookup"><span data-stu-id="a87a8-117">Scope.</span></span>

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

### <span data-ttu-id="a87a8-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a87a8-118">-WorkspaceId</span></span>
<span data-ttu-id="a87a8-119">Arbetsyte-ID.</span><span class="sxs-lookup"><span data-stu-id="a87a8-119">Workspace ID.</span></span>

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

### <span data-ttu-id="a87a8-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a87a8-120">-Confirm</span></span>
<span data-ttu-id="a87a8-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a87a8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a87a8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a87a8-122">-WhatIf</span></span>
<span data-ttu-id="a87a8-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a87a8-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a87a8-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a87a8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a87a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87a8-125">CommonParameters</span></span>
<span data-ttu-id="a87a8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a87a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87a8-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a87a8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87a8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a87a8-128">INPUTS</span></span>

### <span data-ttu-id="a87a8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a87a8-129">System.String</span></span>

## <span data-ttu-id="a87a8-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a87a8-130">OUTPUTS</span></span>

### <span data-ttu-id="a87a8-131">Microsoft. Azure. commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="a87a8-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="a87a8-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a87a8-132">NOTES</span></span>

## <span data-ttu-id="a87a8-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a87a8-133">RELATED LINKS</span></span>
