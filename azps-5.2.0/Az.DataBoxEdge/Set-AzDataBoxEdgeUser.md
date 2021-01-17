---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401776"
---
# <span data-ttu-id="9ca46-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9ca46-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="9ca46-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ca46-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca46-103">Anger ett nytt lösen ord för en användare på enheten.</span><span class="sxs-lookup"><span data-stu-id="9ca46-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="9ca46-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ca46-104">SYNTAX</span></span>

### <span data-ttu-id="9ca46-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9ca46-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca46-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca46-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca46-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca46-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca46-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ca46-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca46-109">Cmdleten **set-AzDataBoxEdgeUser** anger ett nytt lösen ord för en användare i data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="9ca46-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="9ca46-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ca46-110">EXAMPLES</span></span>

### <span data-ttu-id="9ca46-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9ca46-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="9ca46-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ca46-112">PARAMETERS</span></span>

### <span data-ttu-id="9ca46-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ca46-113">-AsJob</span></span>
<span data-ttu-id="9ca46-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9ca46-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ca46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca46-115">-DefaultProfile</span></span>
<span data-ttu-id="9ca46-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca46-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="9ca46-117">-DeviceName</span></span>
<span data-ttu-id="9ca46-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="9ca46-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca46-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9ca46-119">-EncryptionKey</span></span>
<span data-ttu-id="9ca46-120">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="9ca46-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="9ca46-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca46-121">-InputObject</span></span>
<span data-ttu-id="9ca46-122">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="9ca46-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca46-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9ca46-123">-Name</span></span>
<span data-ttu-id="9ca46-124">Namnen</span><span class="sxs-lookup"><span data-stu-id="9ca46-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca46-125">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="9ca46-125">-Password</span></span>
<span data-ttu-id="9ca46-126">Lösen ord, ange som en säker sträng</span><span class="sxs-lookup"><span data-stu-id="9ca46-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="9ca46-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca46-127">-ResourceGroupName</span></span>
<span data-ttu-id="9ca46-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9ca46-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca46-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca46-129">-ResourceId</span></span>
<span data-ttu-id="9ca46-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca46-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca46-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9ca46-131">-Confirm</span></span>
<span data-ttu-id="9ca46-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9ca46-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca46-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca46-133">-WhatIf</span></span>
<span data-ttu-id="9ca46-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9ca46-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ca46-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9ca46-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca46-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca46-136">CommonParameters</span></span>
<span data-ttu-id="9ca46-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ca46-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca46-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ca46-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca46-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ca46-139">INPUTS</span></span>

### <span data-ttu-id="9ca46-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="9ca46-140">None</span></span>

## <span data-ttu-id="9ca46-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ca46-141">OUTPUTS</span></span>

### <span data-ttu-id="9ca46-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9ca46-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="9ca46-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ca46-143">NOTES</span></span>

## <span data-ttu-id="9ca46-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ca46-144">RELATED LINKS</span></span>
