---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410800"
---
# <span data-ttu-id="95caa-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="95caa-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="95caa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95caa-102">SYNOPSIS</span></span>
<span data-ttu-id="95caa-103">Hämtar information om en ögonblicks bild princip för Azure NetApp-filer (ANF).</span><span class="sxs-lookup"><span data-stu-id="95caa-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="95caa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95caa-104">SYNTAX</span></span>

### <span data-ttu-id="95caa-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="95caa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95caa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95caa-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95caa-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95caa-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95caa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95caa-108">DESCRIPTION</span></span>
<span data-ttu-id="95caa-109">Cmdleten **Get-AzNetAppFilesSnapshotPolicy** hämtar information om en ANF-Snapshot-princip.</span><span class="sxs-lookup"><span data-stu-id="95caa-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="95caa-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95caa-110">EXAMPLES</span></span>

### <span data-ttu-id="95caa-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="95caa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="95caa-112">Det här kommandot får säkerhets kopierings principen "MyBackupPolicy" för kontot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="95caa-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="95caa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95caa-113">PARAMETERS</span></span>

### <span data-ttu-id="95caa-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="95caa-114">-AccountName</span></span>
<span data-ttu-id="95caa-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="95caa-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="95caa-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="95caa-116">-AccountObject</span></span>
<span data-ttu-id="95caa-117">Kontot för det nya Snapshot policy-objektet</span><span class="sxs-lookup"><span data-stu-id="95caa-117">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="95caa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95caa-118">-DefaultProfile</span></span>
<span data-ttu-id="95caa-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95caa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95caa-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="95caa-120">-Name</span></span>
<span data-ttu-id="95caa-121">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="95caa-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95caa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95caa-122">-ResourceGroupName</span></span>
<span data-ttu-id="95caa-123">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="95caa-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="95caa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95caa-124">-ResourceId</span></span>
<span data-ttu-id="95caa-125">Resurs-ID för ANF</span><span class="sxs-lookup"><span data-stu-id="95caa-125">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95caa-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="95caa-126">-Confirm</span></span>
<span data-ttu-id="95caa-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95caa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95caa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95caa-128">-WhatIf</span></span>
<span data-ttu-id="95caa-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="95caa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95caa-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="95caa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95caa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95caa-131">CommonParameters</span></span>
<span data-ttu-id="95caa-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95caa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95caa-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95caa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95caa-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95caa-134">INPUTS</span></span>

### <span data-ttu-id="95caa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="95caa-135">System.String</span></span>

### <span data-ttu-id="95caa-136">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="95caa-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="95caa-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95caa-137">OUTPUTS</span></span>

### <span data-ttu-id="95caa-138">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="95caa-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="95caa-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95caa-139">NOTES</span></span>

## <span data-ttu-id="95caa-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95caa-140">RELATED LINKS</span></span>
