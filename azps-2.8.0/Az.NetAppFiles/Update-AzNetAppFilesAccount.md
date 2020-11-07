---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 46415c4d1671c874135b8d754e9217212ade3838
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918585"
---
# <span data-ttu-id="06454-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="06454-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="06454-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06454-102">SYNOPSIS</span></span>
<span data-ttu-id="06454-103">Uppdaterar ett ANF-konto (Azure NetApp-filer) i enlighet med de valfria modifierarna.</span><span class="sxs-lookup"><span data-stu-id="06454-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="06454-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06454-104">SYNTAX</span></span>

```
Update-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```
### <span data-ttu-id="06454-105">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06454-105">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06454-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06454-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06454-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06454-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06454-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06454-108">DESCRIPTION</span></span>
<span data-ttu-id="06454-109">Cmdleten **Update-AzNetAppFilesAccount** ändrar ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="06454-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="06454-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06454-110">EXAMPLES</span></span>

### <span data-ttu-id="06454-111">Exempel 1: uppdaterar ett ANF-konto</span><span class="sxs-lookup"><span data-stu-id="06454-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="06454-112">Det här kommandot utför en uppdatering om det angivna kontot och ändrar taggarna till dem som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="06454-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="06454-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06454-113">PARAMETERS</span></span>

### <span data-ttu-id="06454-114">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="06454-114">-ActiveDirectories</span></span>
<span data-ttu-id="06454-115">En hash-tabell som representerar de aktiva katalogerna</span><span class="sxs-lookup"><span data-stu-id="06454-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06454-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06454-116">-DefaultProfile</span></span>
<span data-ttu-id="06454-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06454-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06454-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06454-118">-InputObject</span></span>
<span data-ttu-id="06454-119">Det konto objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="06454-119">The account object to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06454-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="06454-120">-Location</span></span>
<span data-ttu-id="06454-121">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="06454-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06454-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="06454-122">-Name</span></span>
<span data-ttu-id="06454-123">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="06454-123">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06454-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06454-124">-ResourceGroupName</span></span>
<span data-ttu-id="06454-125">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="06454-125">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06454-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06454-126">-ResourceId</span></span>
<span data-ttu-id="06454-127">Resurs-ID för ANF konto</span><span class="sxs-lookup"><span data-stu-id="06454-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="06454-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="06454-128">-Tag</span></span>
<span data-ttu-id="06454-129">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="06454-129">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06454-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06454-130">-Confirm</span></span>
<span data-ttu-id="06454-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06454-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06454-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06454-132">-WhatIf</span></span>
<span data-ttu-id="06454-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06454-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06454-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06454-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06454-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06454-135">CommonParameters</span></span>
<span data-ttu-id="06454-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06454-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="06454-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06454-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06454-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06454-138">INPUTS</span></span>

### <span data-ttu-id="06454-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="06454-139">None</span></span>

## <span data-ttu-id="06454-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06454-140">OUTPUTS</span></span>

### <span data-ttu-id="06454-141">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="06454-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="06454-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06454-142">NOTES</span></span>

## <span data-ttu-id="06454-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06454-143">RELATED LINKS</span></span>
