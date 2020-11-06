---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 3d2fdd8b6a1763aea97da3967fb2696857e7fd75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579995"
---
# <span data-ttu-id="a5fa3-101">Set-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="a5fa3-101">Set-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="a5fa3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="a5fa3-103">Uppdaterar arbets ytans inställningar för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-103">Updates the workspace settings for the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5fa3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5fa3-104">SYNTAX</span></span>

```
Set-AzureRmSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5fa3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="a5fa3-106">Uppdaterar arbets ytans inställningar för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="a5fa3-107">Den konfigurerade arbets ytan innehåller säkerhets data som samlats in av säkerhets agenten som är installerad på virtuella datorer i det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="a5fa3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5fa3-108">EXAMPLES</span></span>

### <span data-ttu-id="a5fa3-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5fa3-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="a5fa3-110">Ställer in alla säkerhets data som samlats in av säkerhets agenterna i arbets ytan "min arbets yta".</span><span class="sxs-lookup"><span data-stu-id="a5fa3-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="a5fa3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5fa3-111">PARAMETERS</span></span>

### <span data-ttu-id="a5fa3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5fa3-112">-DefaultProfile</span></span>
<span data-ttu-id="a5fa3-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5fa3-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5fa3-114">-Name</span></span>
<span data-ttu-id="a5fa3-115">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-115">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fa3-116">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="a5fa3-116">-Scope</span></span>
<span data-ttu-id="a5fa3-117">Sitt.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-117">Scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fa3-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a5fa3-118">-WorkspaceId</span></span>
<span data-ttu-id="a5fa3-119">Arbetsyte-ID.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-119">Workspace ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5fa3-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5fa3-120">-Confirm</span></span>
<span data-ttu-id="a5fa3-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fa3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5fa3-122">-WhatIf</span></span>
<span data-ttu-id="a5fa3-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5fa3-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5fa3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5fa3-125">CommonParameters</span></span>
<span data-ttu-id="a5fa3-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5fa3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5fa3-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5fa3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5fa3-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5fa3-128">INPUTS</span></span>

### <span data-ttu-id="a5fa3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a5fa3-129">System.String</span></span>

## <span data-ttu-id="a5fa3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5fa3-130">OUTPUTS</span></span>

### <span data-ttu-id="a5fa3-131">Microsoft. Azure. commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="a5fa3-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="a5fa3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5fa3-132">NOTES</span></span>

## <span data-ttu-id="a5fa3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5fa3-133">RELATED LINKS</span></span>
