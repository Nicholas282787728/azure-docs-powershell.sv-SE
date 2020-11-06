---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: e6a47578ef2442e6ca2f6d03284624f1f2906e35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574974"
---
# <span data-ttu-id="08b83-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="08b83-101">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="08b83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08b83-102">SYNOPSIS</span></span>
<span data-ttu-id="08b83-103">Tar bort hot identifierings policyn från en server.</span><span class="sxs-lookup"><span data-stu-id="08b83-103">Removes the threat detection policy from a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08b83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08b83-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08b83-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08b83-105">DESCRIPTION</span></span>
<span data-ttu-id="08b83-106">Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet tar bort hot Detection policyn från en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="08b83-106">The Remove-AzureRmSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>

<span data-ttu-id="08b83-107">Om du vill använda den här cmdleten anger du parametrarna ResourceGroupName och ServerName för att identifiera den server som cmdleten tar bort från.</span><span class="sxs-lookup"><span data-stu-id="08b83-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="08b83-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08b83-108">EXAMPLES</span></span>

### <span data-ttu-id="08b83-109">--------------------------Exempel 1: ta bort en princip för hot identifiering för en databas--------------------------</span><span class="sxs-lookup"><span data-stu-id="08b83-109">--------------------------  Example 1: Remove a threat detection policy for a database  --------------------------</span></span>
```
PS C:\> Remove-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="08b83-110">Det här kommandot tar bort hot identifierings policyn från en server som heter Server01.</span><span class="sxs-lookup"><span data-stu-id="08b83-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="08b83-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08b83-111">PARAMETERS</span></span>

### <span data-ttu-id="08b83-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08b83-112">-PassThru</span></span>
<span data-ttu-id="08b83-113">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="08b83-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="08b83-114">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="08b83-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08b83-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b83-115">-ResourceGroupName</span></span>
<span data-ttu-id="08b83-116">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="08b83-116">Specifies the name of the resource group the server is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08b83-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08b83-117">-ServerName</span></span>
<span data-ttu-id="08b83-118">Anger namnet på en server.</span><span class="sxs-lookup"><span data-stu-id="08b83-118">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08b83-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08b83-119">-Confirm</span></span>
<span data-ttu-id="08b83-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08b83-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08b83-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08b83-121">-WhatIf</span></span>
<span data-ttu-id="08b83-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08b83-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08b83-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08b83-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08b83-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b83-124">-DefaultProfile</span></span>
<span data-ttu-id="08b83-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08b83-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b83-126">CommonParameters</span></span>
<span data-ttu-id="08b83-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08b83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b83-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08b83-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b83-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08b83-129">INPUTS</span></span>

###  
<span data-ttu-id="08b83-130">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08b83-130">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="08b83-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08b83-131">OUTPUTS</span></span>

### <span data-ttu-id="08b83-132">Microsoft. Azure. commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="08b83-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>
<span data-ttu-id="08b83-133">Denna cmdlet returnerar ett ServerThreatDetectionPolicyModel-objekt.</span><span class="sxs-lookup"><span data-stu-id="08b83-133">This cmdlet returns a ServerThreatDetectionPolicyModel object.</span></span>

## <span data-ttu-id="08b83-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08b83-134">NOTES</span></span>

## <span data-ttu-id="08b83-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08b83-135">RELATED LINKS</span></span>

[<span data-ttu-id="08b83-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="08b83-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

