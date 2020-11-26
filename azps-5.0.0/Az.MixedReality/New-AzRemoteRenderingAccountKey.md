---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270540"
---
# <span data-ttu-id="f4a9d-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="f4a9d-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="f4a9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a9d-103">Återskapa nyckeln för fjärrrendering-konto</span><span class="sxs-lookup"><span data-stu-id="f4a9d-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="f4a9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4a9d-104">SYNTAX</span></span>

### <span data-ttu-id="f4a9d-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4a9d-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a9d-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4a9d-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a9d-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4a9d-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a9d-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4a9d-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a9d-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4a9d-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a9d-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4a9d-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a9d-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4a9d-111">DESCRIPTION</span></span>
<span data-ttu-id="f4a9d-112">Återskapa primär nyckeln eller sekundär nyckeln för Remote rendering-konto.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="f4a9d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4a9d-113">EXAMPLES</span></span>

### <span data-ttu-id="f4a9d-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f4a9d-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="f4a9d-115">Återskapa sekundär nyckeln för fjärråter givnings konto "exempel" i resurs gruppen "RG1".</span><span class="sxs-lookup"><span data-stu-id="f4a9d-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="f4a9d-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f4a9d-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="f4a9d-117">Återskapa sekundär nyckeln för fjärråter givnings konto "exempel" från aktuell prenumeration och resurs grupp "RG1" med rör.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="f4a9d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4a9d-118">PARAMETERS</span></span>

### <span data-ttu-id="f4a9d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a9d-119">-DefaultProfile</span></span>
<span data-ttu-id="f4a9d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a9d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f4a9d-121">-Force</span></span>
<span data-ttu-id="f4a9d-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4a9d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4a9d-123">-InputObject</span></span>
<span data-ttu-id="f4a9d-124">Anpassade domän objekt.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a9d-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4a9d-125">-Name</span></span>
<span data-ttu-id="f4a9d-126">Namn på fjärrrendering-konto.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a9d-127">-Primär</span><span class="sxs-lookup"><span data-stu-id="f4a9d-127">-Primary</span></span>
<span data-ttu-id="f4a9d-128">Återskapa primär nyckeln för fjärr åter givnings konto.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a9d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a9d-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4a9d-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a9d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a9d-131">-ResourceId</span></span>
<span data-ttu-id="f4a9d-132">Resurs-ID för fjärrstyrt konto.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4a9d-133">-Sekundär</span><span class="sxs-lookup"><span data-stu-id="f4a9d-133">-Secondary</span></span>
<span data-ttu-id="f4a9d-134">Återskapa primär nyckeln för fjärr åter givnings konto.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a9d-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4a9d-135">-Confirm</span></span>
<span data-ttu-id="f4a9d-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a9d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a9d-137">-WhatIf</span></span>
<span data-ttu-id="f4a9d-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4a9d-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a9d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a9d-140">CommonParameters</span></span>
<span data-ttu-id="f4a9d-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a9d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f4a9d-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a9d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a9d-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4a9d-143">INPUTS</span></span>

### <span data-ttu-id="f4a9d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f4a9d-144">System.String</span></span>

### <span data-ttu-id="f4a9d-145">Microsoft. Azure. commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="f4a9d-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="f4a9d-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4a9d-146">OUTPUTS</span></span>

### <span data-ttu-id="f4a9d-147">Microsoft. Azure. commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f4a9d-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="f4a9d-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4a9d-148">NOTES</span></span>

## <span data-ttu-id="f4a9d-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4a9d-149">RELATED LINKS</span></span>