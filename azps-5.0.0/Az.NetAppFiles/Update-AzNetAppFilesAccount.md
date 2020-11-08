---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 621d4d29d061566e894617d5e918440ba531a041
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263440"
---
# <span data-ttu-id="d66b8-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d66b8-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d66b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d66b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d66b8-103">Uppdaterar ett ANF-konto (Azure NetApp-filer) i enlighet med de valfria modifierarna.</span><span class="sxs-lookup"><span data-stu-id="d66b8-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="d66b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d66b8-104">SYNTAX</span></span>

### <span data-ttu-id="d66b8-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d66b8-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66b8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d66b8-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d66b8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d66b8-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d66b8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d66b8-108">DESCRIPTION</span></span>
<span data-ttu-id="d66b8-109">Cmdleten **Update-AzNetAppFilesAccount** ändrar ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="d66b8-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="d66b8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d66b8-110">EXAMPLES</span></span>

### <span data-ttu-id="d66b8-111">Exempel 1: uppdaterar ett ANF-konto</span><span class="sxs-lookup"><span data-stu-id="d66b8-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="d66b8-112">Det här kommandot utför en uppdatering om det angivna kontot och ändrar taggarna till dem som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="d66b8-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="d66b8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d66b8-113">PARAMETERS</span></span>

### <span data-ttu-id="d66b8-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d66b8-114">-ActiveDirectory</span></span>
<span data-ttu-id="d66b8-115">En hash-tabell som representerar de aktiva katalogerna</span><span class="sxs-lookup"><span data-stu-id="d66b8-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66b8-116">-DefaultProfile</span></span>
<span data-ttu-id="d66b8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d66b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d66b8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d66b8-118">-InputObject</span></span>
<span data-ttu-id="d66b8-119">Det konto objekt som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="d66b8-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d66b8-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="d66b8-120">-Location</span></span>
<span data-ttu-id="d66b8-121">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="d66b8-121">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66b8-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d66b8-122">-Name</span></span>
<span data-ttu-id="d66b8-123">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d66b8-123">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="d66b8-125">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d66b8-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d66b8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d66b8-126">-ResourceId</span></span>
<span data-ttu-id="d66b8-127">Resurs-ID för ANF konto</span><span class="sxs-lookup"><span data-stu-id="d66b8-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="d66b8-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d66b8-128">-Tag</span></span>
<span data-ttu-id="d66b8-129">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="d66b8-129">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66b8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d66b8-130">-Confirm</span></span>
<span data-ttu-id="d66b8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d66b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d66b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66b8-132">-WhatIf</span></span>
<span data-ttu-id="d66b8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d66b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d66b8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d66b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d66b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66b8-135">CommonParameters</span></span>
<span data-ttu-id="d66b8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d66b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66b8-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d66b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66b8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d66b8-138">INPUTS</span></span>

### <span data-ttu-id="d66b8-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="d66b8-139">None</span></span>

## <span data-ttu-id="d66b8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d66b8-140">OUTPUTS</span></span>

### <span data-ttu-id="d66b8-141">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d66b8-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d66b8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d66b8-142">NOTES</span></span>

## <span data-ttu-id="d66b8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d66b8-143">RELATED LINKS</span></span>
