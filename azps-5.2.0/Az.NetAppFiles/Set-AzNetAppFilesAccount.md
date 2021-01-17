---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413568"
---
# <span data-ttu-id="d710a-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d710a-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d710a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d710a-102">SYNOPSIS</span></span>
<span data-ttu-id="d710a-103">Uppdaterar ett Azure NetApp (ANF)-konto med den nya data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d710a-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="d710a-104">Användbart för att ta bort associerade Active kataloger.</span><span class="sxs-lookup"><span data-stu-id="d710a-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="d710a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d710a-105">SYNTAX</span></span>

### <span data-ttu-id="d710a-106">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d710a-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d710a-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d710a-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d710a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d710a-108">DESCRIPTION</span></span>
<span data-ttu-id="d710a-109">Cmdleten **set-AzNetAppFilesAccount** ändrar ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="d710a-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="d710a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d710a-110">EXAMPLES</span></span>

### <span data-ttu-id="d710a-111">Exempel 1: ändra ett ANF-konto</span><span class="sxs-lookup"><span data-stu-id="d710a-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="d710a-112">Det här kommandot utför en uppdatering av det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="d710a-112">This command performs an update on the given account.</span></span> <span data-ttu-id="d710a-113">Om du inte har aktiverat Active Directory kommer det att tas bort från kontot.</span><span class="sxs-lookup"><span data-stu-id="d710a-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="d710a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d710a-114">PARAMETERS</span></span>

### <span data-ttu-id="d710a-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d710a-115">-ActiveDirectory</span></span>
<span data-ttu-id="d710a-116">En hash-tabell som representerar de aktiva katalogerna</span><span class="sxs-lookup"><span data-stu-id="d710a-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d710a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d710a-117">-DefaultProfile</span></span>
<span data-ttu-id="d710a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d710a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d710a-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="d710a-119">-Location</span></span>
<span data-ttu-id="d710a-120">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="d710a-120">The location of the resource</span></span>

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

### <span data-ttu-id="d710a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d710a-121">-Name</span></span>
<span data-ttu-id="d710a-122">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d710a-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="d710a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d710a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d710a-124">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d710a-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d710a-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d710a-125">-Tag</span></span>
<span data-ttu-id="d710a-126">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="d710a-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d710a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d710a-127">-Confirm</span></span>
<span data-ttu-id="d710a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d710a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d710a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d710a-129">-WhatIf</span></span>
<span data-ttu-id="d710a-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d710a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d710a-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d710a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d710a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d710a-132">CommonParameters</span></span>
<span data-ttu-id="d710a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d710a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d710a-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d710a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d710a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d710a-135">INPUTS</span></span>

### <span data-ttu-id="d710a-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="d710a-136">None</span></span>

## <span data-ttu-id="d710a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d710a-137">OUTPUTS</span></span>

### <span data-ttu-id="d710a-138">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d710a-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d710a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d710a-139">NOTES</span></span>

## <span data-ttu-id="d710a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d710a-140">RELATED LINKS</span></span>
