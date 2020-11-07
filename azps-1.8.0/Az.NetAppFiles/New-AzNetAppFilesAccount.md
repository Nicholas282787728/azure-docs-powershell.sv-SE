---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 87febe648a845d595f35c1a14b024fbd97824be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754006"
---
# <span data-ttu-id="ff781-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ff781-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="ff781-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff781-102">SYNOPSIS</span></span>
<span data-ttu-id="ff781-103">Skapar ett nytt Azure NetApp-konto (ANF).</span><span class="sxs-lookup"><span data-stu-id="ff781-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="ff781-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff781-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff781-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff781-105">DESCRIPTION</span></span>
<span data-ttu-id="ff781-106">Cmdleten **New-AzNetAppFilesAccount** skapar ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="ff781-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="ff781-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff781-107">EXAMPLES</span></span>

### <span data-ttu-id="ff781-108">Exempel 1: skapa ett ANF-konto</span><span class="sxs-lookup"><span data-stu-id="ff781-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="ff781-109">Det här kommandot skapar det nya ANF-kontot "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="ff781-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="ff781-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff781-110">PARAMETERS</span></span>

### <span data-ttu-id="ff781-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff781-111">-DefaultProfile</span></span>
<span data-ttu-id="ff781-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff781-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff781-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="ff781-113">-Location</span></span>
<span data-ttu-id="ff781-114">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="ff781-114">The location of the resource</span></span>

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

### <span data-ttu-id="ff781-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff781-115">-Name</span></span>
<span data-ttu-id="ff781-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="ff781-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ff781-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff781-117">-ResourceGroupName</span></span>
<span data-ttu-id="ff781-118">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="ff781-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ff781-119">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ff781-119">-Tag</span></span>
<span data-ttu-id="ff781-120">En hash som representerar resurs koder</span><span class="sxs-lookup"><span data-stu-id="ff781-120">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="ff781-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff781-121">-Confirm</span></span>
<span data-ttu-id="ff781-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff781-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff781-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff781-123">-WhatIf</span></span>
<span data-ttu-id="ff781-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff781-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff781-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff781-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff781-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff781-126">CommonParameters</span></span>
<span data-ttu-id="ff781-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff781-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ff781-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff781-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff781-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff781-129">INPUTS</span></span>

### <span data-ttu-id="ff781-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="ff781-130">None</span></span>

## <span data-ttu-id="ff781-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff781-131">OUTPUTS</span></span>

### <span data-ttu-id="ff781-132">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ff781-132">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="ff781-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff781-133">NOTES</span></span>

## <span data-ttu-id="ff781-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff781-134">RELATED LINKS</span></span>
