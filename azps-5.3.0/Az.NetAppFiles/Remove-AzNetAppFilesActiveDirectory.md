---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7fcf1f749816872fb7407fedaea10d06f3385441
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525882"
---
# <span data-ttu-id="22e57-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="22e57-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="22e57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22e57-102">SYNOPSIS</span></span>
<span data-ttu-id="22e57-103">Tar bort en Azure NetApp-fil (ANF) Active Directory-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="22e57-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="22e57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22e57-104">SYNTAX</span></span>

### <span data-ttu-id="22e57-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="22e57-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22e57-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22e57-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22e57-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22e57-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22e57-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22e57-108">DESCRIPTION</span></span>
<span data-ttu-id="22e57-109">Cmdleten **Remove-AzNetAppFilesActiveDirectory** tar bort en ANF Active Directory-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="22e57-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="22e57-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22e57-110">EXAMPLES</span></span>

### <span data-ttu-id="22e57-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="22e57-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="22e57-112">Detta kommando tar bort den nya Active Directory-ANF med namnet "MyADName".</span><span class="sxs-lookup"><span data-stu-id="22e57-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="22e57-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22e57-113">PARAMETERS</span></span>

### <span data-ttu-id="22e57-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22e57-114">-AccountName</span></span>
<span data-ttu-id="22e57-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="22e57-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e57-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="22e57-116">-AccountObject</span></span>
<span data-ttu-id="22e57-117">Kontot för Active Directory-objektet</span><span class="sxs-lookup"><span data-stu-id="22e57-117">The Account for the Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22e57-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="22e57-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="22e57-119">ID för Active Directory-ANF</span><span class="sxs-lookup"><span data-stu-id="22e57-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e57-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e57-120">-DefaultProfile</span></span>
<span data-ttu-id="22e57-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22e57-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22e57-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22e57-122">-InputObject</span></span>
<span data-ttu-id="22e57-123">Active Directory-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="22e57-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22e57-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22e57-124">-PassThru</span></span>
<span data-ttu-id="22e57-125">Returnera om den angivna Active Directory har tagits bort</span><span class="sxs-lookup"><span data-stu-id="22e57-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="22e57-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e57-126">-ResourceGroupName</span></span>
<span data-ttu-id="22e57-127">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="22e57-127">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e57-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22e57-128">-Confirm</span></span>
<span data-ttu-id="22e57-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22e57-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e57-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e57-130">-WhatIf</span></span>
<span data-ttu-id="22e57-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22e57-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22e57-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22e57-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e57-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e57-133">CommonParameters</span></span>
<span data-ttu-id="22e57-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e57-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e57-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22e57-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e57-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22e57-136">INPUTS</span></span>

### <span data-ttu-id="22e57-137">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="22e57-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="22e57-138">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="22e57-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="22e57-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22e57-139">OUTPUTS</span></span>

### <span data-ttu-id="22e57-140">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="22e57-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="22e57-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22e57-141">NOTES</span></span>

## <span data-ttu-id="22e57-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22e57-142">RELATED LINKS</span></span>
