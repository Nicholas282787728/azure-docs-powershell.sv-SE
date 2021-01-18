---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521028"
---
# <span data-ttu-id="d7913-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d7913-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d7913-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7913-102">SYNOPSIS</span></span>
<span data-ttu-id="d7913-103">Hämtar information om en säkerhets kopierings princip för Azure NetApp-filer (ANF).</span><span class="sxs-lookup"><span data-stu-id="d7913-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="d7913-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7913-104">SYNTAX</span></span>

### <span data-ttu-id="d7913-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d7913-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7913-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7913-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7913-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7913-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7913-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7913-108">DESCRIPTION</span></span>
<span data-ttu-id="d7913-109">Cmdleten **Get-AzNetAppFilesBackupPolicy** hämtar information om en ANF säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="d7913-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="d7913-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7913-110">EXAMPLES</span></span>

### <span data-ttu-id="d7913-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d7913-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="d7913-112">Det här kommandot får säkerhets kopierings principen "MyBackupPolicy" för kontot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="d7913-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="d7913-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7913-113">PARAMETERS</span></span>

### <span data-ttu-id="d7913-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7913-114">-AccountName</span></span>
<span data-ttu-id="d7913-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d7913-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="d7913-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="d7913-116">-AccountObject</span></span>
<span data-ttu-id="d7913-117">Det konto objekt som innehåller säkerhets kopierings principen som ska returneras</span><span class="sxs-lookup"><span data-stu-id="d7913-117">The Account object containing the Backup Policy to return</span></span>

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

### <span data-ttu-id="d7913-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7913-118">-DefaultProfile</span></span>
<span data-ttu-id="d7913-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7913-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7913-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7913-120">-Name</span></span>
<span data-ttu-id="d7913-121">Namnet på ANF säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="d7913-121">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7913-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7913-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7913-123">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d7913-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d7913-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7913-124">-ResourceId</span></span>
<span data-ttu-id="d7913-125">Resurs-ID för ANF säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="d7913-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="d7913-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7913-126">CommonParameters</span></span>
<span data-ttu-id="d7913-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7913-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7913-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7913-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7913-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7913-129">INPUTS</span></span>

### <span data-ttu-id="d7913-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d7913-130">System.String</span></span>

### <span data-ttu-id="d7913-131">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d7913-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d7913-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7913-132">OUTPUTS</span></span>

### <span data-ttu-id="d7913-133">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d7913-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="d7913-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7913-134">NOTES</span></span>

## <span data-ttu-id="d7913-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7913-135">RELATED LINKS</span></span>
