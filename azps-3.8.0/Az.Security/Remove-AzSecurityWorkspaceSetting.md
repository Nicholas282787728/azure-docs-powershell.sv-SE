---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 79780c101296d78115a1c88ef4d4aebcd3721c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089309"
---
# <span data-ttu-id="98125-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="98125-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="98125-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98125-102">SYNOPSIS</span></span>
<span data-ttu-id="98125-103">Tar bort inställningen för säkerhets arbets ytan för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="98125-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="98125-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98125-104">SYNTAX</span></span>

### <span data-ttu-id="98125-105">SubscriptionLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="98125-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98125-106">ID</span><span class="sxs-lookup"><span data-stu-id="98125-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98125-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="98125-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98125-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98125-108">DESCRIPTION</span></span>
<span data-ttu-id="98125-109">Tar bort inställningen för säkerhets arbets ytan för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="98125-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="98125-110">Den här åtgärden gör att de nyligen installerade säkerhets agenterna kan rapportera till standard arbets ytan för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="98125-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="98125-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98125-111">EXAMPLES</span></span>

### <span data-ttu-id="98125-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="98125-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="98125-113">Tar bort inställningen för säkerhets arbets ytan för det här abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="98125-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="98125-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98125-114">PARAMETERS</span></span>

### <span data-ttu-id="98125-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98125-115">-DefaultProfile</span></span>
<span data-ttu-id="98125-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98125-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98125-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98125-117">-InputObject</span></span>
<span data-ttu-id="98125-118">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="98125-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98125-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="98125-119">-Name</span></span>
<span data-ttu-id="98125-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="98125-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98125-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98125-121">-PassThru</span></span>
<span data-ttu-id="98125-122">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="98125-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="98125-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98125-123">-ResourceId</span></span>
<span data-ttu-id="98125-124">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="98125-124">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98125-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98125-125">-Confirm</span></span>
<span data-ttu-id="98125-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98125-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98125-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98125-127">-WhatIf</span></span>
<span data-ttu-id="98125-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98125-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98125-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98125-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98125-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98125-130">CommonParameters</span></span>
<span data-ttu-id="98125-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98125-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98125-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98125-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98125-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98125-133">INPUTS</span></span>

### <span data-ttu-id="98125-134">System. String</span><span class="sxs-lookup"><span data-stu-id="98125-134">System.String</span></span>

### <span data-ttu-id="98125-135">Microsoft. Azure. commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="98125-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="98125-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98125-136">OUTPUTS</span></span>

### <span data-ttu-id="98125-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98125-137">System.Boolean</span></span>

## <span data-ttu-id="98125-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98125-138">NOTES</span></span>

## <span data-ttu-id="98125-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98125-139">RELATED LINKS</span></span>
