---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520995"
---
# <span data-ttu-id="8e81e-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="8e81e-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="8e81e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e81e-102">SYNOPSIS</span></span>
<span data-ttu-id="8e81e-103">Skapar en ny NetApp för Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="8e81e-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="8e81e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e81e-104">SYNTAX</span></span>

### <span data-ttu-id="8e81e-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8e81e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e81e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e81e-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e81e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e81e-107">DESCRIPTION</span></span>
<span data-ttu-id="8e81e-108">Cmdleten **New-AzNetAppFilesBackup** skapar en säkerhets kopia för en ANF volym.</span><span class="sxs-lookup"><span data-stu-id="8e81e-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="8e81e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e81e-109">EXAMPLES</span></span>

### <span data-ttu-id="8e81e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8e81e-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="8e81e-111">Det här kommandot skapar den nya ANF säkerhets kopiering för volymen "volym".</span><span class="sxs-lookup"><span data-stu-id="8e81e-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="8e81e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e81e-112">PARAMETERS</span></span>

### <span data-ttu-id="8e81e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e81e-113">-AccountName</span></span>
<span data-ttu-id="8e81e-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="8e81e-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="8e81e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e81e-115">-DefaultProfile</span></span>
<span data-ttu-id="8e81e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e81e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e81e-117">-Etikett</span><span class="sxs-lookup"><span data-stu-id="8e81e-117">-Label</span></span>
<span data-ttu-id="8e81e-118">Etikett för säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="8e81e-118">Label for backup</span></span>

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

### <span data-ttu-id="8e81e-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="8e81e-119">-Location</span></span>
<span data-ttu-id="8e81e-120">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="8e81e-120">The location of the resource</span></span>

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

### <span data-ttu-id="8e81e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e81e-121">-Name</span></span>
<span data-ttu-id="8e81e-122">Namnet på ANF säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="8e81e-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e81e-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="8e81e-123">-PoolName</span></span>
<span data-ttu-id="8e81e-124">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="8e81e-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8e81e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e81e-125">-ResourceGroupName</span></span>
<span data-ttu-id="8e81e-126">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="8e81e-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8e81e-127">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="8e81e-127">-VolumeName</span></span>
<span data-ttu-id="8e81e-128">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="8e81e-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="8e81e-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="8e81e-129">-VolumeObject</span></span>
<span data-ttu-id="8e81e-130">Volymen för det nya säkerhetskopierade objektet</span><span class="sxs-lookup"><span data-stu-id="8e81e-130">The volume for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e81e-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e81e-131">-Confirm</span></span>
<span data-ttu-id="8e81e-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e81e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e81e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e81e-133">-WhatIf</span></span>
<span data-ttu-id="8e81e-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e81e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e81e-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e81e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e81e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e81e-136">CommonParameters</span></span>
<span data-ttu-id="8e81e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e81e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e81e-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e81e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e81e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e81e-139">INPUTS</span></span>

### <span data-ttu-id="8e81e-140">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8e81e-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="8e81e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e81e-141">OUTPUTS</span></span>

### <span data-ttu-id="8e81e-142">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="8e81e-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="8e81e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e81e-143">NOTES</span></span>

## <span data-ttu-id="8e81e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e81e-144">RELATED LINKS</span></span>
