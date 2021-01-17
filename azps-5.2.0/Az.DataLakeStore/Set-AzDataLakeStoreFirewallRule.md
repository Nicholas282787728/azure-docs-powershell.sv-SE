---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413371"
---
# <span data-ttu-id="654a8-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="654a8-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="654a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="654a8-102">SYNOPSIS</span></span>
<span data-ttu-id="654a8-103">Ändrar den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="654a8-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="654a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="654a8-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="654a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="654a8-105">DESCRIPTION</span></span>
<span data-ttu-id="654a8-106">Cmdleten **set-AzDataLakeStoreFirewallRule** ändrar den angivna brand Väggs regeln i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="654a8-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="654a8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="654a8-107">EXAMPLES</span></span>

### <span data-ttu-id="654a8-108">Exempel 1: Uppdatera start-och slut adress för en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="654a8-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="654a8-109">Uppdaterar brand Väggs regeln "MyFirewallRule" i kontot "ContosoADL" för att ha ett område med 127.0.0.1-127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="654a8-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="654a8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="654a8-110">PARAMETERS</span></span>

### <span data-ttu-id="654a8-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="654a8-111">-Account</span></span>
<span data-ttu-id="654a8-112">Data Lake Store-konto för att uppdatera brand Väggs regeln i</span><span class="sxs-lookup"><span data-stu-id="654a8-112">The Data Lake Store account to update the firewall rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="654a8-113">-DefaultProfile</span></span>
<span data-ttu-id="654a8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="654a8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="654a8-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="654a8-115">-EndIpAddress</span></span>
<span data-ttu-id="654a8-116">Slutet på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="654a8-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654a8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="654a8-117">-Name</span></span>
<span data-ttu-id="654a8-118">Namnet på brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="654a8-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="654a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="654a8-120">Anger namnet på den resurs grupp som innehåller kontot som ska uppdatera brand Väggs regeln för.</span><span class="sxs-lookup"><span data-stu-id="654a8-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654a8-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="654a8-121">-StartIpAddress</span></span>
<span data-ttu-id="654a8-122">Början på det giltiga IP-intervallet för brand Väggs regeln</span><span class="sxs-lookup"><span data-stu-id="654a8-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654a8-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="654a8-123">-Confirm</span></span>
<span data-ttu-id="654a8-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="654a8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="654a8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="654a8-125">-WhatIf</span></span>
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

### <span data-ttu-id="654a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="654a8-126">CommonParameters</span></span>
<span data-ttu-id="654a8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="654a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="654a8-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="654a8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="654a8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="654a8-129">INPUTS</span></span>

### <span data-ttu-id="654a8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="654a8-130">System.String</span></span>

## <span data-ttu-id="654a8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="654a8-131">OUTPUTS</span></span>

### <span data-ttu-id="654a8-132">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="654a8-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="654a8-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="654a8-133">NOTES</span></span>

## <span data-ttu-id="654a8-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="654a8-134">RELATED LINKS</span></span>
