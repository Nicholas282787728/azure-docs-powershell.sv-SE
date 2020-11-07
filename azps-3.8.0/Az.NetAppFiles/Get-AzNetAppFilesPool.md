---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 613f9b2703dcdf16a6f4d87dd1cdc4c8938c1bad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925646"
---
# <span data-ttu-id="89246-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="89246-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="89246-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89246-102">SYNOPSIS</span></span>
<span data-ttu-id="89246-103">Hämtar information om en ANF-pool (Azure NetApp-filer).</span><span class="sxs-lookup"><span data-stu-id="89246-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="89246-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89246-104">SYNTAX</span></span>

### <span data-ttu-id="89246-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="89246-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89246-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89246-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89246-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89246-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89246-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89246-108">DESCRIPTION</span></span>
<span data-ttu-id="89246-109">Cmdleten **Get-AzNetAppFilesPool** hämtar information om en ANF-pool.</span><span class="sxs-lookup"><span data-stu-id="89246-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="89246-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89246-110">EXAMPLES</span></span>

### <span data-ttu-id="89246-111">Exempel 1: skaffa en ANF-pool</span><span class="sxs-lookup"><span data-stu-id="89246-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="89246-112">Det här kommandot får kontot MyAnfPool från kontot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="89246-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="89246-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89246-113">PARAMETERS</span></span>

### <span data-ttu-id="89246-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89246-114">-AccountName</span></span>
<span data-ttu-id="89246-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="89246-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89246-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="89246-116">-AccountObject</span></span>
<span data-ttu-id="89246-117">Det konto objekt som innehåller poolen som ska returneras</span><span class="sxs-lookup"><span data-stu-id="89246-117">The account object containing the pool to return</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89246-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89246-118">-DefaultProfile</span></span>
<span data-ttu-id="89246-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89246-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89246-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="89246-120">-Name</span></span>
<span data-ttu-id="89246-121">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="89246-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89246-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89246-122">-ResourceGroupName</span></span>
<span data-ttu-id="89246-123">ANF resurs grupp</span><span class="sxs-lookup"><span data-stu-id="89246-123">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89246-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89246-124">-ResourceId</span></span>
<span data-ttu-id="89246-125">Resurs-ID för ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="89246-125">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89246-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89246-126">CommonParameters</span></span>
<span data-ttu-id="89246-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89246-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="89246-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89246-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89246-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89246-129">INPUTS</span></span>

### <span data-ttu-id="89246-130">System. String</span><span class="sxs-lookup"><span data-stu-id="89246-130">System.String</span></span>

### <span data-ttu-id="89246-131">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="89246-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="89246-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89246-132">OUTPUTS</span></span>

### <span data-ttu-id="89246-133">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="89246-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="89246-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89246-134">NOTES</span></span>

## <span data-ttu-id="89246-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89246-135">RELATED LINKS</span></span>
