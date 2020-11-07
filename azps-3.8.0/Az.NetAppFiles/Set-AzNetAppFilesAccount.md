---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: d2a379567ab96f5776b55c4cfbac2eabeaeb02a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925609"
---
# <span data-ttu-id="652bd-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="652bd-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="652bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="652bd-102">SYNOPSIS</span></span>
<span data-ttu-id="652bd-103">Uppdaterar ett Azure NetApp (ANF)-konto med den nya data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="652bd-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="652bd-104">Användbart för att ta bort associerade Active kataloger.</span><span class="sxs-lookup"><span data-stu-id="652bd-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="652bd-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="652bd-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="652bd-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="652bd-106">DESCRIPTION</span></span>
<span data-ttu-id="652bd-107">Cmdleten **set-AzNetAppFilesAccount** ändrar ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="652bd-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="652bd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="652bd-108">EXAMPLES</span></span>

### <span data-ttu-id="652bd-109">Exempel 1: ändra ett ANF-konto</span><span class="sxs-lookup"><span data-stu-id="652bd-109">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="652bd-110">Det här kommandot utför en uppdatering av det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="652bd-110">This command performs an update on the given account.</span></span> <span data-ttu-id="652bd-111">Om du inte har aktiverat Active Directory kommer det att tas bort från kontot.</span><span class="sxs-lookup"><span data-stu-id="652bd-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="652bd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="652bd-112">PARAMETERS</span></span>

### <span data-ttu-id="652bd-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="652bd-113">-ActiveDirectories</span></span>
<span data-ttu-id="652bd-114">En hash-tabell som representerar de aktiva katalogerna</span><span class="sxs-lookup"><span data-stu-id="652bd-114">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="652bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="652bd-115">-DefaultProfile</span></span>
<span data-ttu-id="652bd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="652bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="652bd-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="652bd-117">-Location</span></span>
<span data-ttu-id="652bd-118">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="652bd-118">The location of the resource</span></span>

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

### <span data-ttu-id="652bd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="652bd-119">-Name</span></span>
<span data-ttu-id="652bd-120">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="652bd-120">The name of the ANF account</span></span>

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

### <span data-ttu-id="652bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="652bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="652bd-122">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="652bd-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="652bd-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="652bd-123">-Tag</span></span>
<span data-ttu-id="652bd-124">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="652bd-124">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="652bd-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="652bd-125">-Confirm</span></span>
<span data-ttu-id="652bd-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="652bd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="652bd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="652bd-127">-WhatIf</span></span>
<span data-ttu-id="652bd-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="652bd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="652bd-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="652bd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="652bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="652bd-130">CommonParameters</span></span>
<span data-ttu-id="652bd-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="652bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="652bd-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="652bd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="652bd-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="652bd-133">INPUTS</span></span>

### <span data-ttu-id="652bd-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="652bd-134">None</span></span>

## <span data-ttu-id="652bd-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="652bd-135">OUTPUTS</span></span>

### <span data-ttu-id="652bd-136">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="652bd-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="652bd-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="652bd-137">NOTES</span></span>

## <span data-ttu-id="652bd-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="652bd-138">RELATED LINKS</span></span>
