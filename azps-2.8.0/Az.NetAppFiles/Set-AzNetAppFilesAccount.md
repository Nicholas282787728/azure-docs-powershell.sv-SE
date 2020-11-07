---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: 873b506ea1fd50e2869a19a45a302c5fe12a781b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918865"
---
# <span data-ttu-id="d8e57-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d8e57-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d8e57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8e57-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e57-103">Uppdaterar ett Azure NetApp (ANF)-konto med den nya data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d8e57-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="d8e57-104">Användbart för att ta bort associerade Active kataloger.</span><span class="sxs-lookup"><span data-stu-id="d8e57-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="d8e57-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8e57-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e57-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8e57-106">DESCRIPTION</span></span>
<span data-ttu-id="d8e57-107">Cmdleten **set-AzNetAppFilesAccount** ändrar ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="d8e57-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="d8e57-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8e57-108">EXAMPLES</span></span>

### <span data-ttu-id="d8e57-109">Exempel 1: ändra ett ANF-konto</span><span class="sxs-lookup"><span data-stu-id="d8e57-109">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="d8e57-110">Det här kommandot utför en uppdatering av det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="d8e57-110">This command performs an update on the given account.</span></span> <span data-ttu-id="d8e57-111">Om du inte har aktiverat Active Directory kommer det att tas bort från kontot.</span><span class="sxs-lookup"><span data-stu-id="d8e57-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="d8e57-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8e57-112">PARAMETERS</span></span>

### <span data-ttu-id="d8e57-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="d8e57-113">-ActiveDirectories</span></span>
<span data-ttu-id="d8e57-114">En hash-tabell som representerar de aktiva katalogerna</span><span class="sxs-lookup"><span data-stu-id="d8e57-114">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="d8e57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e57-115">-DefaultProfile</span></span>
<span data-ttu-id="d8e57-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d8e57-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8e57-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="d8e57-117">-Location</span></span>
<span data-ttu-id="d8e57-118">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="d8e57-118">The location of the resource</span></span>

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

### <span data-ttu-id="d8e57-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8e57-119">-Name</span></span>
<span data-ttu-id="d8e57-120">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d8e57-120">The name of the ANF account</span></span>

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

### <span data-ttu-id="d8e57-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e57-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8e57-122">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d8e57-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d8e57-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d8e57-123">-Tag</span></span>
<span data-ttu-id="d8e57-124">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="d8e57-124">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d8e57-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8e57-125">-Confirm</span></span>
<span data-ttu-id="d8e57-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8e57-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e57-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e57-127">-WhatIf</span></span>
<span data-ttu-id="d8e57-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8e57-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e57-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8e57-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e57-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e57-130">CommonParameters</span></span>
<span data-ttu-id="d8e57-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e57-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d8e57-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e57-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e57-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8e57-133">INPUTS</span></span>

### <span data-ttu-id="d8e57-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="d8e57-134">None</span></span>

## <span data-ttu-id="d8e57-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8e57-135">OUTPUTS</span></span>

### <span data-ttu-id="d8e57-136">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d8e57-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d8e57-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8e57-137">NOTES</span></span>

## <span data-ttu-id="d8e57-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8e57-138">RELATED LINKS</span></span>
