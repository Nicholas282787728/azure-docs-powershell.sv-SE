---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410712"
---
# <span data-ttu-id="f7784-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f7784-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="f7784-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7784-102">SYNOPSIS</span></span>
<span data-ttu-id="f7784-103">Tar bort ett Azure NetApp (ANF)-konto.</span><span class="sxs-lookup"><span data-stu-id="f7784-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="f7784-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7784-104">SYNTAX</span></span>

### <span data-ttu-id="f7784-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f7784-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7784-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7784-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7784-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7784-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7784-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7784-108">DESCRIPTION</span></span>
<span data-ttu-id="f7784-109">Cmdleten **Remove-AzNetAppFilesAccount** tar bort ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="f7784-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="f7784-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7784-110">EXAMPLES</span></span>

### <span data-ttu-id="f7784-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f7784-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="f7784-112">Det här kommandot tar bort ANF-kontot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="f7784-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="f7784-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7784-113">PARAMETERS</span></span>

### <span data-ttu-id="f7784-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7784-114">-DefaultProfile</span></span>
<span data-ttu-id="f7784-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7784-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7784-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7784-116">-InputObject</span></span>
<span data-ttu-id="f7784-117">Det konto objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="f7784-117">The account object to remove</span></span>

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

### <span data-ttu-id="f7784-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7784-118">-Name</span></span>
<span data-ttu-id="f7784-119">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="f7784-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7784-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7784-120">-PassThru</span></span>
<span data-ttu-id="f7784-121">Returnera om det angivna kontot har tagits bort</span><span class="sxs-lookup"><span data-stu-id="f7784-121">Return whether the specified account was successfully removed</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7784-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7784-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7784-123">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="f7784-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f7784-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7784-124">-ResourceId</span></span>
<span data-ttu-id="f7784-125">Resurs-ID för ANF konto</span><span class="sxs-lookup"><span data-stu-id="f7784-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="f7784-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7784-126">-Confirm</span></span>
<span data-ttu-id="f7784-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7784-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7784-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7784-128">-WhatIf</span></span>
<span data-ttu-id="f7784-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7784-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7784-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7784-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7784-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7784-131">CommonParameters</span></span>
<span data-ttu-id="f7784-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7784-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7784-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7784-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7784-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7784-134">INPUTS</span></span>

### <span data-ttu-id="f7784-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f7784-135">System.String</span></span>

### <span data-ttu-id="f7784-136">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="f7784-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="f7784-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7784-137">OUTPUTS</span></span>

### <span data-ttu-id="f7784-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7784-138">System.Boolean</span></span>

## <span data-ttu-id="f7784-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7784-139">NOTES</span></span>

## <span data-ttu-id="f7784-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7784-140">RELATED LINKS</span></span>
