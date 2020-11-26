---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1c649a63e8ba57a3d2e9f9af28e0ce4b12ca9a0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260028"
---
# <span data-ttu-id="cd17f-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cd17f-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="cd17f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd17f-102">SYNOPSIS</span></span>
<span data-ttu-id="cd17f-103">Ändrar den angivna regeln för virtuella nätverk i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cd17f-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="cd17f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd17f-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd17f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd17f-105">DESCRIPTION</span></span>
<span data-ttu-id="cd17f-106">Cmdleten **set-AzDataLakeStoreVirtualNetworkRule** ändrar den angivna regeln för virtuella nätverk i den angivna data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cd17f-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="cd17f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd17f-107">EXAMPLES</span></span>

### <span data-ttu-id="cd17f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd17f-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="cd17f-109">Uppdaterar under nätets ID för regeln "myVNET" i kontot "DLS" till "updatedId"</span><span class="sxs-lookup"><span data-stu-id="cd17f-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="cd17f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd17f-110">PARAMETERS</span></span>

### <span data-ttu-id="cd17f-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="cd17f-111">-Account</span></span>
<span data-ttu-id="cd17f-112">Kontot för data Lake Store för att uppdatera regeln för virtuella nätverk i</span><span class="sxs-lookup"><span data-stu-id="cd17f-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="cd17f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd17f-113">-DefaultProfile</span></span>
<span data-ttu-id="cd17f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd17f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd17f-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd17f-115">-Name</span></span>
<span data-ttu-id="cd17f-116">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="cd17f-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="cd17f-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cd17f-117">-SubnetId</span></span>
<span data-ttu-id="cd17f-118">Början på det giltiga IP-adressintervallet för regeln för virtuella nätverk</span><span class="sxs-lookup"><span data-stu-id="cd17f-118">The start of the valid ip range for the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd17f-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd17f-119">-Confirm</span></span>
<span data-ttu-id="cd17f-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd17f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd17f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd17f-121">-WhatIf</span></span>
<span data-ttu-id="cd17f-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd17f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd17f-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd17f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd17f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd17f-124">CommonParameters</span></span>
<span data-ttu-id="cd17f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd17f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd17f-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd17f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd17f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd17f-127">INPUTS</span></span>

### <span data-ttu-id="cd17f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cd17f-128">System.String</span></span>

## <span data-ttu-id="cd17f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd17f-129">OUTPUTS</span></span>

### <span data-ttu-id="cd17f-130">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cd17f-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="cd17f-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd17f-131">NOTES</span></span>

## <span data-ttu-id="cd17f-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd17f-132">RELATED LINKS</span></span>