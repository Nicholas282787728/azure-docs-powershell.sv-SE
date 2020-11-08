---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 257421a43c3da11c82316eaf58d2983fe47d5f05
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270843"
---
# <span data-ttu-id="7639e-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7639e-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="7639e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7639e-102">SYNOPSIS</span></span>
<span data-ttu-id="7639e-103">Hämtar information om en ANF-pool (Azure NetApp-filer).</span><span class="sxs-lookup"><span data-stu-id="7639e-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="7639e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7639e-104">SYNTAX</span></span>

### <span data-ttu-id="7639e-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7639e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7639e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7639e-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7639e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7639e-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7639e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7639e-108">DESCRIPTION</span></span>
<span data-ttu-id="7639e-109">Cmdleten **Get-AzNetAppFilesPool** hämtar information om en ANF-pool.</span><span class="sxs-lookup"><span data-stu-id="7639e-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="7639e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7639e-110">EXAMPLES</span></span>

### <span data-ttu-id="7639e-111">Exempel 1: skaffa en ANF-pool</span><span class="sxs-lookup"><span data-stu-id="7639e-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="7639e-112">Det här kommandot får kontot MyAnfPool från kontot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="7639e-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="7639e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7639e-113">PARAMETERS</span></span>

### <span data-ttu-id="7639e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7639e-114">-AccountName</span></span>
<span data-ttu-id="7639e-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="7639e-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="7639e-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="7639e-116">-AccountObject</span></span>
<span data-ttu-id="7639e-117">Det konto objekt som innehåller poolen som ska returneras</span><span class="sxs-lookup"><span data-stu-id="7639e-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="7639e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7639e-118">-DefaultProfile</span></span>
<span data-ttu-id="7639e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7639e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7639e-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="7639e-120">-Name</span></span>
<span data-ttu-id="7639e-121">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="7639e-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7639e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7639e-122">-ResourceGroupName</span></span>
<span data-ttu-id="7639e-123">ANF resurs grupp</span><span class="sxs-lookup"><span data-stu-id="7639e-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="7639e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7639e-124">-ResourceId</span></span>
<span data-ttu-id="7639e-125">Resurs-ID för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="7639e-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="7639e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7639e-126">CommonParameters</span></span>
<span data-ttu-id="7639e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7639e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7639e-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7639e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7639e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7639e-129">INPUTS</span></span>

### <span data-ttu-id="7639e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7639e-130">System.String</span></span>

### <span data-ttu-id="7639e-131">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7639e-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="7639e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7639e-132">OUTPUTS</span></span>

### <span data-ttu-id="7639e-133">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="7639e-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="7639e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7639e-134">NOTES</span></span>

## <span data-ttu-id="7639e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7639e-135">RELATED LINKS</span></span>
