---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260922"
---
# <span data-ttu-id="6d636-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="6d636-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="6d636-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d636-102">SYNOPSIS</span></span>
<span data-ttu-id="6d636-103">Anger ett nytt lösen ord för en användare på enheten.</span><span class="sxs-lookup"><span data-stu-id="6d636-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="6d636-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d636-104">SYNTAX</span></span>

### <span data-ttu-id="6d636-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6d636-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d636-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d636-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d636-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d636-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d636-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d636-108">DESCRIPTION</span></span>
<span data-ttu-id="6d636-109">Cmdleten **set-AzStackEdgeUser** anger ett nytt lösen ord för en användare på stack Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="6d636-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="6d636-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d636-110">EXAMPLES</span></span>

### <span data-ttu-id="6d636-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6d636-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="6d636-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d636-112">PARAMETERS</span></span>

### <span data-ttu-id="6d636-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d636-113">-AsJob</span></span>
<span data-ttu-id="6d636-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6d636-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d636-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d636-115">-DefaultProfile</span></span>
<span data-ttu-id="6d636-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d636-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d636-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="6d636-117">-DeviceName</span></span>
<span data-ttu-id="6d636-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="6d636-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d636-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6d636-119">-EncryptionKey</span></span>
<span data-ttu-id="6d636-120">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="6d636-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d636-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d636-121">-InputObject</span></span>
<span data-ttu-id="6d636-122">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="6d636-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d636-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d636-123">-Name</span></span>
<span data-ttu-id="6d636-124">Namnen</span><span class="sxs-lookup"><span data-stu-id="6d636-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d636-125">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="6d636-125">-Password</span></span>
<span data-ttu-id="6d636-126">Lösen ord, ange som en säker sträng</span><span class="sxs-lookup"><span data-stu-id="6d636-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d636-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d636-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d636-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6d636-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d636-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d636-129">-ResourceId</span></span>
<span data-ttu-id="6d636-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d636-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d636-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d636-131">-Confirm</span></span>
<span data-ttu-id="6d636-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d636-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d636-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d636-133">-WhatIf</span></span>
<span data-ttu-id="6d636-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d636-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d636-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d636-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d636-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d636-136">CommonParameters</span></span>
<span data-ttu-id="6d636-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d636-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d636-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d636-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d636-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d636-139">INPUTS</span></span>

### <span data-ttu-id="6d636-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="6d636-140">None</span></span>

## <span data-ttu-id="6d636-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d636-141">OUTPUTS</span></span>

### <span data-ttu-id="6d636-142">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="6d636-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="6d636-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d636-143">NOTES</span></span>

## <span data-ttu-id="6d636-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d636-144">RELATED LINKS</span></span>
