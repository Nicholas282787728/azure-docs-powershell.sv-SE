---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 8b533f26b7fa947a185ee0be2dc5a395e77ebbbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578196"
---
# <span data-ttu-id="3be6c-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3be6c-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="3be6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3be6c-102">SYNOPSIS</span></span>
<span data-ttu-id="3be6c-103">Tar bort en tilldelad identitet.</span><span class="sxs-lookup"><span data-stu-id="3be6c-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3be6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3be6c-104">SYNTAX</span></span>

### <span data-ttu-id="3be6c-105">ResourceGroupAndNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3be6c-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3be6c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3be6c-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3be6c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3be6c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3be6c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3be6c-108">DESCRIPTION</span></span>
<span data-ttu-id="3be6c-109">**Remove-AzureRmUserAssignedIdentity** tar bort den angivna användarens identitet.</span><span class="sxs-lookup"><span data-stu-id="3be6c-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="3be6c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3be6c-110">EXAMPLES</span></span>

### <span data-ttu-id="3be6c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3be6c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="3be6c-112">Med den här cmdleten tar du bort identiteten **id1** under resurs grupp **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="3be6c-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>

<span data-ttu-id="3be6c-113">Sant</span><span class="sxs-lookup"><span data-stu-id="3be6c-113">True</span></span>

## <span data-ttu-id="3be6c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3be6c-114">PARAMETERS</span></span>

### <span data-ttu-id="3be6c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3be6c-115">-AsJob</span></span>
<span data-ttu-id="3be6c-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3be6c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3be6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be6c-117">-DefaultProfile</span></span>
<span data-ttu-id="3be6c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3be6c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3be6c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3be6c-119">-Force</span></span>
<span data-ttu-id="3be6c-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="3be6c-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="3be6c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3be6c-121">-InputObject</span></span>
<span data-ttu-id="3be6c-122">Identity-objektet.</span><span class="sxs-lookup"><span data-stu-id="3be6c-122">The Identity object.</span></span>

```yaml
Type: PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3be6c-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="3be6c-123">-Name</span></span>
<span data-ttu-id="3be6c-124">Identitets namnet.</span><span class="sxs-lookup"><span data-stu-id="3be6c-124">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be6c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3be6c-125">-ResourceGroupName</span></span>
<span data-ttu-id="3be6c-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3be6c-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be6c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3be6c-127">-ResourceId</span></span>
<span data-ttu-id="3be6c-128">Identitetens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3be6c-128">The Identity's resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3be6c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3be6c-129">-Confirm</span></span>
<span data-ttu-id="3be6c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3be6c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3be6c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3be6c-131">-WhatIf</span></span>
<span data-ttu-id="3be6c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3be6c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3be6c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3be6c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3be6c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be6c-134">CommonParameters</span></span>
<span data-ttu-id="3be6c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be6c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be6c-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be6c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be6c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3be6c-137">INPUTS</span></span>

### <span data-ttu-id="3be6c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3be6c-138">System.String</span></span>

## <span data-ttu-id="3be6c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3be6c-139">OUTPUTS</span></span>

### <span data-ttu-id="3be6c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3be6c-140">System.Boolean</span></span>

## <span data-ttu-id="3be6c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3be6c-141">NOTES</span></span>

## <span data-ttu-id="3be6c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3be6c-142">RELATED LINKS</span></span>
