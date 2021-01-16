---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410832"
---
# <span data-ttu-id="dba0e-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="dba0e-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="dba0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dba0e-102">SYNOPSIS</span></span>
<span data-ttu-id="dba0e-103">Hämtar information om en ANF-säkerhetskopia (Azure NetApp-filer).</span><span class="sxs-lookup"><span data-stu-id="dba0e-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="dba0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dba0e-104">SYNTAX</span></span>

### <span data-ttu-id="dba0e-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dba0e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dba0e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba0e-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dba0e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba0e-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dba0e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dba0e-108">DESCRIPTION</span></span>
<span data-ttu-id="dba0e-109">Cmdleten **Get-AzNetAppFilesBackup** hämtar information om en ANF säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="dba0e-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="dba0e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dba0e-110">EXAMPLES</span></span>

### <span data-ttu-id="dba0e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dba0e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="dba0e-112">Det här kommandot får backcup med namnet "MyAnfAccount" från volymen "volym".</span><span class="sxs-lookup"><span data-stu-id="dba0e-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="dba0e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dba0e-113">PARAMETERS</span></span>

### <span data-ttu-id="dba0e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dba0e-114">-AccountName</span></span>
<span data-ttu-id="dba0e-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="dba0e-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="dba0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba0e-116">-DefaultProfile</span></span>
<span data-ttu-id="dba0e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dba0e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba0e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="dba0e-118">-Name</span></span>
<span data-ttu-id="dba0e-119">Namnet på ANF säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="dba0e-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dba0e-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="dba0e-120">-PoolName</span></span>
<span data-ttu-id="dba0e-121">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="dba0e-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="dba0e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba0e-122">-ResourceGroupName</span></span>
<span data-ttu-id="dba0e-123">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="dba0e-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="dba0e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dba0e-124">-ResourceId</span></span>
<span data-ttu-id="dba0e-125">Resurs-ID för ANF säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="dba0e-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="dba0e-126">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="dba0e-126">-VolumeName</span></span>
<span data-ttu-id="dba0e-127">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="dba0e-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dba0e-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="dba0e-128">-VolumeObject</span></span>
<span data-ttu-id="dba0e-129">Volym objekt som innehåller säkerhets kopian som ska returneras</span><span class="sxs-lookup"><span data-stu-id="dba0e-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="dba0e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba0e-130">CommonParameters</span></span>
<span data-ttu-id="dba0e-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba0e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba0e-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dba0e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba0e-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dba0e-133">INPUTS</span></span>

### <span data-ttu-id="dba0e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dba0e-134">System.String</span></span>

### <span data-ttu-id="dba0e-135">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="dba0e-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="dba0e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dba0e-136">OUTPUTS</span></span>

### <span data-ttu-id="dba0e-137">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="dba0e-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="dba0e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dba0e-138">NOTES</span></span>

## <span data-ttu-id="dba0e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dba0e-139">RELATED LINKS</span></span>
