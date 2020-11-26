---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270827"
---
# <span data-ttu-id="d2ee7-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d2ee7-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="d2ee7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ee7-103">Skapar ett nytt Azure NetApp-konto (ANF).</span><span class="sxs-lookup"><span data-stu-id="d2ee7-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="d2ee7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2ee7-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ee7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2ee7-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ee7-106">Cmdleten **New-AzNetAppFilesAccount** skapar ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="d2ee7-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="d2ee7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2ee7-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ee7-108">Exempel 1: skapa ett ANF-konto</span><span class="sxs-lookup"><span data-stu-id="d2ee7-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="d2ee7-109">Det här kommandot skapar det nya ANF-kontot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="d2ee7-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="d2ee7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2ee7-110">PARAMETERS</span></span>

### <span data-ttu-id="d2ee7-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d2ee7-111">-ActiveDirectory</span></span>
<span data-ttu-id="d2ee7-112">En hash-tabell som representerar de aktiva katalogerna</span><span class="sxs-lookup"><span data-stu-id="d2ee7-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="d2ee7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ee7-113">-DefaultProfile</span></span>
<span data-ttu-id="d2ee7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ee7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2ee7-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="d2ee7-115">-Location</span></span>
<span data-ttu-id="d2ee7-116">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="d2ee7-116">The location of the resource</span></span>

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

### <span data-ttu-id="d2ee7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2ee7-117">-Name</span></span>
<span data-ttu-id="d2ee7-118">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d2ee7-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="d2ee7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ee7-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2ee7-120">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="d2ee7-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d2ee7-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d2ee7-121">-Tag</span></span>
<span data-ttu-id="d2ee7-122">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="d2ee7-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d2ee7-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d2ee7-123">-Confirm</span></span>
<span data-ttu-id="d2ee7-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2ee7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ee7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ee7-125">-WhatIf</span></span>
<span data-ttu-id="d2ee7-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d2ee7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ee7-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d2ee7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ee7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ee7-128">CommonParameters</span></span>
<span data-ttu-id="d2ee7-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ee7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ee7-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2ee7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ee7-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2ee7-131">INPUTS</span></span>

### <span data-ttu-id="d2ee7-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="d2ee7-132">None</span></span>

## <span data-ttu-id="d2ee7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2ee7-133">OUTPUTS</span></span>

### <span data-ttu-id="d2ee7-134">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d2ee7-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d2ee7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2ee7-135">NOTES</span></span>

## <span data-ttu-id="d2ee7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2ee7-136">RELATED LINKS</span></span>