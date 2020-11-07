---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: c344d5ac901e45c92c04a23cee252b1f747d4a83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922978"
---
# <span data-ttu-id="e1a19-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="e1a19-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="e1a19-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1a19-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a19-103">Anger ett nytt lösen ord för en användare på enheten.</span><span class="sxs-lookup"><span data-stu-id="e1a19-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="e1a19-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1a19-104">SYNTAX</span></span>

### <span data-ttu-id="e1a19-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e1a19-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1a19-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1a19-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1a19-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1a19-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1a19-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1a19-108">DESCRIPTION</span></span>
<span data-ttu-id="e1a19-109">Cmdleten **set-AzDataBoxEdgeUser** anger ett nytt lösen ord för en användare i data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="e1a19-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="e1a19-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1a19-110">EXAMPLES</span></span>

### <span data-ttu-id="e1a19-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e1a19-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="e1a19-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1a19-112">PARAMETERS</span></span>

### <span data-ttu-id="e1a19-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1a19-113">-AsJob</span></span>
<span data-ttu-id="e1a19-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e1a19-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1a19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a19-115">-DefaultProfile</span></span>
<span data-ttu-id="e1a19-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1a19-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1a19-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="e1a19-117">-DeviceName</span></span>
<span data-ttu-id="e1a19-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="e1a19-118">Device Name</span></span>

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

### <span data-ttu-id="e1a19-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e1a19-119">-EncryptionKey</span></span>
<span data-ttu-id="e1a19-120">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="e1a19-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="e1a19-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1a19-121">-InputObject</span></span>
<span data-ttu-id="e1a19-122">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="e1a19-122">Input Object</span></span>

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

### <span data-ttu-id="e1a19-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1a19-123">-Name</span></span>
<span data-ttu-id="e1a19-124">Namnen</span><span class="sxs-lookup"><span data-stu-id="e1a19-124">Username</span></span>

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

### <span data-ttu-id="e1a19-125">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="e1a19-125">-Password</span></span>
<span data-ttu-id="e1a19-126">Lösen ord, ange som en säker sträng</span><span class="sxs-lookup"><span data-stu-id="e1a19-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="e1a19-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1a19-127">-ResourceGroupName</span></span>
<span data-ttu-id="e1a19-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e1a19-128">Resource Group Name</span></span>

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

### <span data-ttu-id="e1a19-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1a19-129">-ResourceId</span></span>
<span data-ttu-id="e1a19-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1a19-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="e1a19-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1a19-131">-Confirm</span></span>
<span data-ttu-id="e1a19-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1a19-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1a19-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1a19-133">-WhatIf</span></span>
<span data-ttu-id="e1a19-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1a19-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1a19-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1a19-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1a19-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a19-136">CommonParameters</span></span>
<span data-ttu-id="e1a19-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1a19-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a19-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1a19-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a19-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1a19-139">INPUTS</span></span>

### <span data-ttu-id="e1a19-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="e1a19-140">None</span></span>

## <span data-ttu-id="e1a19-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1a19-141">OUTPUTS</span></span>

### <span data-ttu-id="e1a19-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="e1a19-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="e1a19-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1a19-143">NOTES</span></span>

## <span data-ttu-id="e1a19-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1a19-144">RELATED LINKS</span></span>
